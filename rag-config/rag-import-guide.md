# AI 向量知识库导入指南

## 概述

本指南说明如何将本知识库的文档导入 AI 向量数据库（如 Dify、AnythingLLM、LangChain 等），实现语义检索问答。

## 一、数据来源

- **仅读取** `docs/` 目录下的所有 Markdown 文档
- **忽略** `raw-material/` 目录（这是草稿，不参与检索）
- **忽略** 配置文件（mkdocs.yml、.gitignore 等）

## 二、文档切片规则

### 切片方式

按二级标题（`##`）切割分段。每个二级标题下的内容为一段。

例如 `[堆肥与有机肥](docs/agriculture/compost-fertilizer.md)` 按以下段落切割：

```
段落1: 现代底层原理（简化）
段落2: 古代实操完整步骤
段落3: 优势对比（对比古代现有技术）
段落4: 局限性与短板
段落5: 拓展延伸配套技术
```

### 字数限制

- 每段目标字数：500-1200 字
- 如果某段不足 500 字，可以与上一段合并
- 如果某段超过 1200 字，需要手动再细分

### 元数据附加

每段切片需要附加以下元数据：

```json
{
  "source": "文档路径",
  "分类": "农业/医疗/日用化工/冶金/建筑/数理/长期工业/避坑",
  "落地难度": "当日落地/1个月可量产/完整产业链（数年）",
  "标签": ["#标签1", "#标签2"]
}
```

## 三、检索权重配置

### 权重分配

| 分类 | 权重 | 说明 |
|------|------|------|
| 医疗防疫 | 1.5 | 生存刚需，优先展示 |
| 农业增产 | 1.3 | 生存刚需 |
| 日用化工 | 1.2 | 生活必需 |
| 冶金锻造 | 1.0 | 基础工业 |
| 建筑机械 | 1.0 | 基础建设 |
| 数理测绘 | 1.0 | 基础工具 |
| 长期工业 | 0.7 | 需要完整产业链，权重降低 |
| 避坑合集 | 0.5（负面） | 用于过滤不现实的回答 |

### 避坑文档用法

当用户提问涉及以下领域时，系统应自动检查避坑文档：
- 电力、电子、通信 → 引用 [electric-tech.md](../docs/limits/electric-tech.md)
- 精密机械、塑料、橡胶 → 引用 [high-precision.md](../docs/limits/high-precision.md)
- 现代金融、法律、互联网 → 引用 [modern-system.md](../docs/limits/modern-system.md)

如果用户的提问涉及这些领域，AI 应在回答中提醒："该技术需要现代工业体系支撑，在古代条件下无法实现。"

## 四、问答提示词模板

```
你是一个穿越古代技术顾问。请严格基于以下知识库内容回答问题：

【知识库内容】
{context}

【回答规则】
1. 只使用知识库中明确提到的技术
2. 区分技术的落地难度（当日落地 / 1个月可量产 / 完整产业链）
3. 如果问题涉及的知识不在知识库中，诚实告知"知识库中没有相关内容"
4. 如果问题涉及的技术在古代无法实现，引用避坑文档进行提醒
5. 回答中使用通俗易懂的语言，避免现代专业术语
6. 给出具体可操作的步骤，不要只讲理论
7. 在回答末尾附上相关文档的跳转链接
```

## 五、各平台导入方法

### Dify

1. 登录 Dify 控制台
2. 创建一个新的"知识库"
3. 上传 `docs/` 目录下所有 `.md` 文件
4. 分段模式选择"自定义"，分段长度设为 1000 字符
5. 索引模式选择"质量优先"
6. 保存后等待索引完成

### AnythingLLM

1. 打开 AnythingLLM 管理面板
2. 创建新的 Workspace
3. 在"Documents"中选择"Upload Files"
4. 上传 `docs/` 目录下所有 `.md` 文件
5. 分割器选择"Markdown Headers"
6. 嵌入模型选择 `all-MiniLM-L6-v2`（中文效果尚可）或多语言模型
7. 保存并等待索引完成

### LangChain + ChromaDB（本地部署）

```python
from langchain.document_loaders import DirectoryLoader, MarkdownLoader
from langchain.text_splitter import MarkdownHeaderTextSplitter
from langchain.embeddings import HuggingFaceEmbeddings
from langchain.vectorstores import Chroma

# 加载文档
loader = DirectoryLoader('docs/', glob='**/*.md', loader_cls=MarkdownLoader)
documents = loader.load()

# 切片
splitter = MarkdownHeaderTextSplitter(
    headers_to_split_on=[("#", "Header 1"), ("##", "Header 2")]
)
chunks = []
for doc in documents:
    chunks.extend(splitter.split_text(doc.page_content))

# 创建向量库
embeddings = HuggingFaceEmbeddings(model_name="sentence-transformers/all-MiniLM-L6-v2")
vectorstore = Chroma.from_documents(chunks, embeddings, persist_directory="./chroma_db")

# 持久化
vectorstore.persist()
```

## 六、后续维护

1. **定期同步**：每当 `docs/` 目录有新文档或更新时，重新导入向量库
2. **质量监控**：定期检查检索结果的相关性
3. **反馈收集**：记录用户不满意的答案，针对性补充知识库内容
4. **切片优化**：根据检索效果调整切片策略
