# 🏮 穿越古代现代技术知识库

> **无电力依赖、古代可复刻的现代知识合集**
>
> 分类整理农业、医疗、化工、冶金、工程、数理等可复刻技术，区分落地难度与资源门槛，支持静态文档网页浏览与 AI RAG 语义检索。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-中文-red.svg)]()
[![MkDocs](https://img.shields.io/badge/docs-MkDocs%20Material-blue.svg)](https://www.mkdocs.org/)

---

## 📌 项目定位

| 定位 | 说明 |
|------|------|
| **资料存档** | Git 版本管理，持续迭代补充知识点 |
| **在线文档** | MkDocs Material 生成美观静态知识库网页，GitHub Pages 免费部署 |
| **AI 检索兼容** | 所有文档标准化切片，可一键导入 Dify / AnythingLLM 做专属问答机器人 |
| **使用人群** | 网文写作参考、穿越题材设定参考、古代低成本复刻技术研究 |

## 🚀 快速开始

### 在线阅读

部署完成后，可通过浏览器访问静态文档站点（替换为你的 GitHub 用户名）：

```
https://<your-username>.github.io/time-travel-tech-knowledge-base/
```

### 本地预览

```bash
# 安装 MkDocs Material 主题
pip install mkdocs-material

# 启动本地预览服务器
mkdocs serve

# 在浏览器打开 http://localhost:8000
```

### 部署到 GitHub Pages

```bash
# 编辑 mkdocs.yml 中的 site_url 为你的仓库地址
# 然后部署
mkdocs gh-deploy
```

## 📖 知识库导航

### 🌾 农业增产 — 当日即可落地

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [堆肥与有机肥](docs/agriculture/compost-fertilizer.md) | 当日落地 | #低成本手工 #增产 |
| [作物育种与人工授粉](docs/agriculture/seed-breeding.md) | 当日落地 | #低成本手工 #增产 |
| [简易水利灌溉](docs/agriculture/irrigation.md) | 当日落地 | #基建改造 #无电力 |
| [土法防虫](docs/agriculture/pest-control.md) | 当日落地 | #低成本手工 #防疫 |

### 🏥 医疗防疫急救 — 救人性命

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [消毒杀菌基础](docs/medical-health/disinfection.md) | 当日落地 | #防疫 #医疗救人 |
| [大规模瘟疫防控](docs/medical-health/plague-prevent.md) | 1个月可量产 | #防疫 #医疗救人 |
| [通用现场急救](docs/medical-health/first-aid.md) | 当日落地 | #医疗救人 #低成本手工 |
| [缺维生素对应食疗](docs/medical-health/nutrition-deficiency.md) | 当日落地 | #医疗救人 #低成本手工 |

### ⚗️ 日用简易化工 — 短期可量产

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [土法制肥皂](docs/daily-chemistry/soap-make.md) | 1个月可量产 | #低成本手工 #高收益 |
| [草木灰提取碱水](docs/daily-chemistry/alkali-extract.md) | 1个月可量产 | #低成本手工 #高收益 |
| [白糖脱色提纯](docs/daily-chemistry/sugar-refine.md) | 1个月可量产 | #低成本手工 #高收益 |
| [明矾净水工艺](docs/daily-chemistry/alum-water-purify.md) | 当日落地 | #防疫 #低成本手工 |
| [标准安全黑火药](docs/daily-chemistry/black-powder.md) | 1个月可量产 | #高收益 #官府建功 |

### 🔩 冶金锻造改良

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [改良高炉炼铁](docs/metallurgy-forging/blast-furnace-improve.md) | 1个月可量产 | #基建改造 #高收益 |
| [铁器淬火回火](docs/metallurgy-forging/quenching-temper.md) | 1个月可量产 | #高收益 |
| [青铜黄铜合金配比](docs/metallurgy-forging/bronze-alloy.md) | 1个月可量产 | #高收益 #官府建功 |

### 🏗️ 建筑与机械力学

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [土法防水水泥](docs/architecture-mechanic/ancient-concrete.md) | 1个月可量产 | #基建改造 |
| [拱桥与承重结构](docs/architecture-mechanic/arch-structure.md) | 1个月可量产 | #基建改造 |
| [水车与省力滑轮](docs/architecture-mechanic/water-mill-upgrade.md) | 当日落地 | #基建改造 #无电力 |

### 📐 测绘数理记账

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [阿拉伯数字速算](docs/math-measurement/arab-numbers.md) | 当日落地 | #低成本手工 |
| [勾股测距测地](docs/math-measurement/pythagoras-measure.md) | 当日落地 | #低成本手工 |
| [统计台账管理](docs/math-measurement/statistics-manage.md) | 当日落地 | #低成本手工 |

### 🏭 长期工业技术（多年布局）

| 技术 | 落地难度 | 标签 |
|------|----------|------|
| [土法蒸馏酸碱](docs/long-term-industry/vitriol-distill.md) | 完整产业链（数年） | #高收益 |
| [简易铜锌电池](docs/long-term-industry/volta-battery.md) | 完整产业链（数年） | #高收益 |
| [蒸汽机原理与瓶颈](docs/long-term-industry/steam-theory.md) | 完整产业链（数年） | #基建改造 |

### ⚠️ 古代无法实现技术避坑

| 技术 | 说明 |
|------|------|
| [电力芯片相关全部作废](docs/limits/electric-tech.md) | 凡需电力、半导体、电机的技术均不可行 |
| [精密机械高分子材料](docs/limits/high-precision.md) | 精密机床、内燃机、塑料橡胶等无法复刻 |
| [现代社会体系无法落地](docs/limits/modern-system.md) | 现代金融、法律、互联网体系不具备落地条件 |

## 🤖 AI 检索 / RAG 知识库

本知识库的文档经过标准化处理，可直接导入 AI 向量数据库进行语义检索问答。

### 快速接入

1. 将 `docs/` 目录下所有 Markdown 文档导出
2. 参考 **[rag-config/rag-import-guide.md](rag-config/rag-import-guide.md)** 导入 Dify / AnythingLLM
3. 文档按二级标题切片，每段 500–1200 字，已标注落地难度标签

### 检索权重策略

- 医疗、农业（生存刚需）权重最高
- 日用化工次之
- 长期工业技术权重降低
- 避坑文档用于负面过滤，回答时自动提醒限制条件

详见 [rag-config/doc-slice-rule.md](rag-config/doc-slice-rule.md)。

## 📁 仓库结构

```
time-travel-tech-knowledge-base/
├── docs/                   # 核心文档（MkDocs 编译输出）
│   ├── index.md            # 知识库首页
│   ├── roadmap.md          # 穿越分阶段落地路线
│   ├── agriculture/        # 农业类
│   ├── medical-health/     # 医疗防疫类
│   ├── daily-chemistry/    # 日用化工类
│   ├── metallurgy-forging/ # 冶金锻造类
│   ├── architecture-mechanic/ # 建筑机械类
│   ├── math-measurement/   # 数理测绘类
│   ├── long-term-industry/ # 长期工业类
│   ├── limits/             # 避坑合集
│   └── assets/             # 图片与示意图
├── raw-material/           # 原始草稿与参考资料（不对外展示）
├── rag-config/             # AI 向量知识库配置说明
├── mkdocs.yml              # 静态网站配置
├── .gitignore              # Git 忽略规则
├── LICENSE                 # MIT 协议
└── README.md               # 本文件
```

## ✍️ 文档规范

所有技术文档统一遵循以下格式：

```markdown
# 文档标题
## 基础元数据
- 分类：xxx
- 落地难度：当日落地 / 1个月可量产 / 完整产业链（数年）
- 必备原料：xxx
- 是否需要特殊工具：是 / 否
- 适用场景：生存致富 / 官府建功 / 基建改造 / 医疗救人
- 标签：#xxx

## 一、现代底层原理（简化）
## 二、古代实操完整步骤
## 三、优势对比
## 四、局限性与短板
## 五、拓展延伸配套技术
```

详细规范见 [dev.md](dev.md)。

## 📝 贡献指南

欢迎任何形式的贡献：

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/amazing-doc`)
3. 提交改动 (`git commit -m '添加一篇精彩的技术文档'`)
4. 推送到分支 (`git push origin feature/amazing-doc`)
5. 提交 Pull Request

### 新增文档 checklist

- [ ] 遵循统一文档头部元数据模板
- [ ] 在 `mkdocs.yml` 的 `nav` 中添加导航条目
- [ ] 文档内添加跨文档跳转链接（`../` 相对路径）
- [ ] 涉及图片时在 `docs/assets/` 下放置，并在文中引用

## 📄 开源协议

本项目采用 [MIT 协议](LICENSE) — 可以自由复制、二次修改、商用，无需保留版权声明（但建议保留以示尊重）。

---

> 💡 **提示**：本知识库所有内容仅供网文创作参考、历史技术研究与教育用途。部分技术（如黑火药）在现实中可能受到法律法规严格管制，请勿在实际生活中违规操作。
