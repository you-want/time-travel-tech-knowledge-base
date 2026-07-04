# 穿越古代实用现代技术知识库 GitHub 完整项目规划模板
可直接复制给大模型，一键生成整套仓库目录、模板文件、配置、文档规范，分三大部分：仓库基础信息、完整目录结构、统一文档规范、MkDocs 部署配置、AI RAG 配套说明、README 首页文案。

## 一、仓库基础元信息（给AI生成项目时先复制这段）
### 仓库名称
`time-travel-tech-knowledge-base`
### 仓库简介
一套可落地、无电力依赖、适配古代生产力的现代知识知识库，分类整理农业、医疗、化工、冶金、工程、数理等可复刻技术，区分落地难度与资源门槛，支持静态文档网页、可接入RAG大模型语义检索。
### 开源协议
MIT（自由复制、二次修改、商用无限制）
### 项目定位
1. 资料存档：Git 版本管理，持续迭代补充知识点
2. 在线文档：MkDocs Material 生成美观静态知识库网页，GitHub Pages 免费部署
3. AI 检索兼容：所有文档标准化切片，可一键导入 Dify / AnythingLLM 做专属问答机器人
4. 使用人群：网文写作参考、穿越题材设定参考、古代低成本复刻技术研究

## 二、完整仓库树形目录（AI 严格按此生成文件）
```
time-travel-tech-knowledge-base/
├── README.md                     # 仓库首页总介绍、导航、使用指南
├── mkdocs.yml                    # 静态文档网站全局配置
├── .gitignore                    # Git忽略文件配置
├── LICENSE                       # MIT开源协议
├── docs/                         # MkDocs网页核心文档（全部对外展示内容）
│   ├── index.md                  # 知识库首页
│   ├── roadmap.md                # 穿越分阶段落地路线（初期/中期/长期）
│   ├── limits/                   # 古代无法实现的现代技术避坑合集
│   │   ├── electric-tech.md      # 电力/芯片/电机相关全部作废技术
│   │   ├── high-precision.md     # 精密机床、内燃机、高分子材料等
│   │   └── modern-system.md      # 现代金融、法律、互联网体系
│   ├── agriculture/              # 农业类：当日即可落地
│   │   ├── compost-fertilizer.md # 堆肥、秸秆还田、固氮作物
│   │   ├── seed-breeding.md      # 人工选种、果树人工授粉
│   │   ├── irrigation.md         # 简易水利、梯田、浅层打井
│   │   └── pest-control.md       # 草木灰、烟草水土法驱虫
│   ├── medical-health/           # 防疫、急救、卫生、营养学
│   │   ├── disinfection.md       # 煮沸消毒、生石灰伤口处理
│   │   ├── plague-prevent.md     # 瘟疫隔离、水源管控防疫体系
│   │   ├── first-aid.md          # 骨折、出血、中暑、食物中毒急救
│   │   └── nutrition-deficiency.md # 夜盲、坏血病对应食疗方案
│   ├── daily-chemistry/          # 草木/矿物简易化工，短期可量产
│   │   ├── soap-make.md          # 油脂+草木灰土法制皂
│   │   ├── alkali-extract.md     # 草木灰提取纯碱、烧碱
│   │   ├── sugar-refine.md       # 土法脱色精制白糖
│   │   ├── alum-water-purify.md  # 明矾净水工艺
│   │   └── black-powder.md       # 标准配比黑火药制作与安全规范
│   ├── metallurgy-forging/       # 炼铁、炼钢、金属改良
│   │   ├── blast-furnace-improve.md # 改良鼓风炼铁
│   │   ├── quenching-temper.md   # 铁器淬火回火工艺
│   │   └── bronze-alloy.md       # 铜锡锌合金配比优化
│   ├── architecture-mechanic/    # 建筑、水利机械、力学
│   │   ├── ancient-concrete.md   # 石灰炉渣防水土水泥
│   │   ├── arch-structure.md     # 拱桥、承重墙体力学设计
│   │   └── water-mill-upgrade.md # 多级水车、滑轮省力结构
│   ├── math-measurement/         # 数理、测绘、记账工具
│   │   ├── arab-numbers.md       # 阿拉伯数字、速算、小数分数
│   │   ├── pythagoras-measure.md # 勾股丈量土地、测距测高
│   │   └── statistics-manage.md  # 人口粮食统计、制表管理
│   ├── long-term-industry/       # 需要完整产业链，数年才能落地
│   │   ├── vitriol-distill.md    # 土法蒸馏硫酸、硝酸
│   │   ├── volta-battery.md      # 铜锌盐水简易电池
│   │   └── steam-theory.md       # 蒸汽机理论与古代制造瓶颈
│   └── assets/                   # 图片、流程图、工艺示意图
│       ├── agriculture/
│       ├── chemical/
│       └── metallurgy/
├── raw-material/                 # 原始草稿、零散素材、摘抄资料（不参与网页编译）
│   ├── temp-notes.md
│   └── reference-collect.md
└── rag-config/                   # AI向量知识库配套切片规则、导入说明
    ├── rag-import-guide.md
    └── doc-slice-rule.md
```

## 三、统一文档写作标准（所有md文件强制遵守，方便AI检索）
每一篇技术文档固定头部模板，AI读取时可自动分类、提取标签、判断落地难度
### 单文件标准头部模板（复制给AI，每篇文档开头必须加）
```markdown
# 文档标题
## 基础元数据
- 分类：农业/医疗/日用化工/冶金/建筑/数理/长期工业/不可实现技术
- 落地难度：当日落地 / 1个月可量产 / 完整产业链（数年）
- 必备原料：XXX、XXX（仅古代天然矿物、动植物）
- 是否需要特殊工具：是/否
- 适用场景：生存致富、官府建功、基建改造、医疗救人
- 标签：#低成本手工 #无电力 #高收益 #防疫 #增产

## 一、现代底层原理（简化，无现代专业术语）
直白讲清楚科学逻辑，不出现化学分子式、物理公式等超古代理解内容

## 二、古代实操完整步骤
分1、2、3步，纯人力、土设备可完成

## 三、优势对比（对比古代现有技术）
1. 产量提升XX%
2. 成本降低
3. 风险降低（瘟疫、农具损坏等）

## 四、局限性与短板
古代缺少什么资源会限制效果，有什么副作用、风险

## 五、拓展延伸配套技术
和本技术联动的其他知识点，做内部文档跳转链接
```

## 四、mkdocs.yml 完整配置（直接生成，MkDocs静态网站）
```yaml
site_name: 穿越古代现代技术知识库
site_description: 无电力、古代可复刻现代知识合集，农业医疗化工冶金工程全套
site_author: TimeTravel Tech
site_url: https://你的github用户名.github.io/time-travel-tech-knowledge-base

theme:
  name: material
  language: zh
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.top
    - search.suggest
    - search.highlight
  palette:
    - scheme: default
      primary: blue
      accent: cyan
    - scheme: slate
      primary: blue
      accent: cyan

plugins:
  - search:
      lang: zh

nav:
  - 首页: index.md
  - 落地总路线: roadmap.md
  - 农业增产:
      - 堆肥与有机肥: agriculture/compost-fertilizer.md
      - 作物育种人工授粉: agriculture/seed-breeding.md
      - 简易水利灌溉: agriculture/irrigation.md
      - 土法防虫: agriculture/pest-control.md
  - 医疗防疫急救:
      - 消毒杀菌基础: medical-health/disinfection.md
      - 大规模瘟疫防控: medical-health/plague-prevent.md
      - 通用现场急救: medical-health/first-aid.md
      - 缺维生素对应食疗: medical-health/nutrition-deficiency.md
  - 日用简易化工:
      - 土法制肥皂: daily-chemistry/soap-make.md
      - 草木灰提取碱水: daily-chemistry/alkali-extract.md
      - 白糖脱色提纯: daily-chemistry/sugar-refine.md
      - 明矾净水工艺: daily-chemistry/alum-water-purify.md
      - 标准安全黑火药: daily-chemistry/black-powder.md
  - 冶金锻造改良:
      - 改良高炉炼铁: metallurgy-forging/blast-furnace-improve.md
      - 铁器淬火回火: metallurgy-forging/quenching-temper.md
      - 青铜黄铜合金配比: metallurgy-forging/bronze-alloy.md
  - 建筑与机械力学:
      - 土法防水水泥: architecture-mechanic/ancient-concrete.md
      - 拱桥与承重结构: architecture-mechanic/arch-structure.md
      - 水车与省力滑轮: architecture-mechanic/water-mill-upgrade.md
  - 测绘数理记账:
      - 阿拉伯数字速算: math-measurement/arab-numbers.md
      - 勾股测距测地: math-measurement/pythagoras-measure.md
      - 统计台账管理: math-measurement/statistics-manage.md
  - 长期工业技术（多年布局）:
      - 土法蒸馏酸碱: long-term-industry/vitriol-distill.md
      - 简易铜锌电池: long-term-industry/volta-battery.md
      - 蒸汽机原理与瓶颈: long-term-industry/steam-theory.md
  - 古代无法实现技术避坑:
      - 电力芯片相关全部作废: limits/electric-tech.md
      - 精密机械高分子材料: limits/high-precision.md
      - 现代社会体系无法落地: limits/modern-system.md
```

## 五、.gitignore 标准文件内容
```
# 本地编辑器缓存
.obsidian/
.typora/
# Python缓存（MkDocs运行产生）
__pycache__/
*.pyc
# 生成静态网站文件
site/
# 本地大模型向量缓存
vector-cache/
# 系统文件
.DS_Store
Thumbs.db
# 环境密钥
.env
```

## 六、配套RAG AI知识库使用规则（rag-config/rag-import-guide.md核心内容）
1. 仅读取 `/docs` 下所有md文档，忽略raw-material草稿
2. 切片规则：单篇文档按二级标题 ## 切割分段，每段500–1200字
3. 检索权重：
   - 医疗、农业（生存刚需）权重最高
   - 长期工业技术权重降低
   - limits 避坑文档用于负面过滤，回答时自动提醒限制条件
4. 问答提示词固定模板：以知识库内容为唯一依据，区分技术落地难度，不编造古代不存在材料

## 七、给AI生成项目的完整指令（你直接复制发给大模型）
> 请根据下面完整仓库规划，生成一套完整 GitHub 项目文件：
> 1. 仓库名 time-travel-tech-knowledge-base，MIT协议
> 2. 严格按照给定树形目录创建全部md文档、配置文件
> 3. 所有技术文档统一使用规定头部元数据模板，语言通俗易懂，无复杂现代专业术语，适配穿越古代场景
> 4. 自动填充每一份文档完整内容，步骤清晰，区分原理、实操、优缺点、配套关联技术
> 5. 输出完整文件分块，每个文件标注路径+完整文本内容
> 6. 附带 mkdocs.yml、.gitignore、LICENSE、README 全部完整配置文本
> 7. 文档内添加内部跳转链接，方便知识库互相引用

## 八、后续操作流程（生成完项目后执行）
1. 本地新建文件夹，按AI输出全部文件创建完整目录
2. 初始化 Git，推送至 GitHub 新建仓库
3. 本地安装 MkDocs：`pip install mkdocs-material`
4. 本地预览网页：`mkdocs serve`
5. 部署 GitHub Pages 实现在线公开文档站
6. 将 `/docs` 全部文档导入 AnythingLLM / Dify，搭建专属AI检索问答知识库

需要我直接把**完整仓库README首页成品文案**一次性写给你吗？