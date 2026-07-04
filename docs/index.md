<style>
/* 首页古风卡片样式 */
.knowledge-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.2em;
  margin: 1.5em 0;
}

.knowledge-card {
  border: 1px solid #D4C5A9;
  border-radius: 6px;
  padding: 1.2em;
  background: rgba(253, 246, 236, 0.6);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.knowledge-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(to right, #C41E3A, #B8860B);
}

.knowledge-card:hover {
  border-color: #C41E3A;
  box-shadow: 0 4px 12px rgba(44, 24, 16, 0.1);
  transform: translateY(-2px);
}

.knowledge-card .card-icon {
  font-size: 1.8em;
  margin-bottom: 0.5em;
  display: block;
}

.knowledge-card .card-title {
  font-size: 1.1em;
  font-weight: 600;
  color: #2C1810;
  margin-bottom: 0.5em;
  letter-spacing: 0.03em;
}

.knowledge-card .card-desc {
  font-size: 0.9em;
  color: #5A4A3A;
  line-height: 1.6;
}

.knowledge-card .card-tags {
  margin-top: 0.8em;
  display: flex;
  flex-wrap: wrap;
  gap: 0.3em;
}

.knowledge-card .tag {
  font-size: 0.75em;
  padding: 0.15em 0.5em;
  border-radius: 3px;
  background: rgba(184, 134, 11, 0.1);
  color: #8B4513;
  border: 1px solid rgba(184, 134, 11, 0.2);
}

/* 难度徽章 */
.difficulty-badge {
  display: inline-block;
  font-size: 0.75em;
  padding: 0.15em 0.6em;
  border-radius: 10px;
  margin-left: 0.5em;
  vertical-align: middle;
}

.diff-easy {
  background: rgba(34, 139, 34, 0.1);
  color: #228B22;
  border: 1px solid rgba(34, 139, 34, 0.3);
}

.diff-medium {
  background: rgba(184, 134, 11, 0.1);
  color: #8B4513;
  border: 1px solid rgba(184, 134, 11, 0.3);
}

.diff-hard {
  background: rgba(196, 30, 58, 0.1);
  color: #C41E3A;
  border: 1px solid rgba(196, 30, 58, 0.3);
}

.diff-impossible {
  background: rgba(128, 0, 128, 0.1);
  color: #800080;
  border: 1px solid rgba(128, 0, 128, 0.3);
}
</style>

<div class="hero-banner">
<h1>🏮 穿越古代现代技术知识库</h1>
<p class="subtitle">无电力依赖 · 古代可复刻 · 现代知识合集</p>
</div>

> 如果你突然回到了古代（或者正在写穿越小说、做穿越题材设定），你会面临一个核心问题：**现代有哪些技术不需要电力和精密仪器，仅凭古代已有的材料和人力就能复刻？**
>
> 本知识库就是为了解答这个问题而生。

<div class="quick-links">
<a href="roadmap.md" class="quick-link">🗺️ 落地路线</a>
<a href="#农桑" class="quick-link">🌾 农桑</a>
<a href="#医理" class="quick-link">🏥 医理</a>
<a href="#百工" class="quick-link">⚗️ 百工</a>
<a href="#避坑" class="quick-link">⚠️ 避坑指南</a>
<a href="rag-config/rag-import-guide.html" class="quick-link">🤖 AI 检索</a>
</div>

---

## 📊 技术分级总览

我们将所有技术按落地难度分为三个等级：

| 等级 | 说明 | 代表技术 |
|------|------|----------|
| **当日落地** <span class="difficulty-badge diff-easy">易</span> | 掌握原理后立刻可以动手做 | 堆肥、净水、消毒、阿拉伯数字 |
| **一月量产** <span class="difficulty-badge diff-medium">中</span> | 需要搭建简易工坊、积累原料 | 制皂、提碱、炼铁、黑火药 |
| **数年远工** <span class="difficulty-badge diff-hard">难</span> | 需要完整工业体系支撑 | 蒸馏酸碱、电池、蒸汽机 |

另有大量现代技术**在古代根本无法实现**，我们专门整理了避坑合集，帮你排除无效思路。

---

## 🗂️ 知识库分类

### 农桑 <a id="农桑"></a>

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🌱</span>
<div class="card-title">堆肥与有机肥</div>
<div class="card-desc">草木秸秆变沃土，微生物"慢炖锅"原理</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#增产</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🌾</span>
<div class="card-title">作物育种与人工授粉</div>
<div class="card-desc">三年选种出良种，人工授粉翻倍产</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#增产</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">💧</span>
<div class="card-title">简易水利灌溉</div>
<div class="card-desc">引水渠、梯田、手摇井，把水送到庄稼边</div>
<div class="card-tags"><span class="tag">当日~一月</span><span class="tag">#基建</span><span class="tag">#无电力</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🐛</span>
<div class="card-title">土法防虫</div>
<div class="card-desc">草木灰、烟草水、辣椒蒜，天然驱虫不伤土</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#防疫</span><span class="tag">#低成本</span></div>
</div>
</div>

### 医理 <a id="医理"></a>

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🔥</span>
<div class="card-title">消毒杀菌基础</div>
<div class="card-desc">煮沸消毒、生石灰处理，两大法宝防感染</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#防疫</span><span class="tag">#救命</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🏚️</span>
<div class="card-title">大规模瘟疫防控</div>
<div class="card-desc">隔离制度、水源管控、灭虫防疫体系</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#防疫</span><span class="tag">#救命</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🩹</span>
<div class="card-title">通用现场急救</div>
<div class="card-desc">止血、骨折固定、中暑、食物中毒急救</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#救命</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🥣</span>
<div class="card-title">缺维生素对应食疗</div>
<div class="card-desc">夜盲、坏血病、脚气病，吃什么补什么</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#救命</span><span class="tag">#低成本</span></div>
</div>
</div>

### 百工 <a id="百工"></a>

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🧼</span>
<div class="card-title">土法制肥皂</div>
<div class="card-desc">油脂 + 草木灰 = 既能洗脸又能洗衣的宝贝</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🧪</span>
<div class="card-title">草木灰提取碱水</div>
<div class="card-desc">化工之母，制皂、洗衣、食品加工样样行</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🍬</span>
<div class="card-title">白糖脱色提纯</div>
<div class="card-desc">红糖变白糖，骨炭吸附，价值翻倍</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🫗</span>
<div class="card-title">明矾净水工艺</div>
<div class="card-desc">一撮明矾，浑水变清，饮水安全第一步</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#防疫</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">💥</span>
<div class="card-title">标准安全黑火药</div>
<div class="card-desc">一硝二磺三木炭，军事采矿双用途</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#官府建功</span></div>
</div>
</div>

### 冶铸

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🔨</span>
<div class="card-title">改良高炉炼铁</div>
<div class="card-desc">鼓风炼铁，产量翻倍，质量提升</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#基建</span><span class="tag">#高收益</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">⚒️</span>
<div class="card-title">铁器淬火回火</div>
<div class="card-desc">烧红水冷再回温，铁器硬度翻倍不脆断</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#官府建功</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🪙</span>
<div class="card-title">青铜黄铜合金配比</div>
<div class="card-desc">铜锡锌黄金比例，兵器货币皆可用</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#高收益</span><span class="tag">#官府建功</span></div>
</div>
</div>

### 营造

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🏗️</span>
<div class="card-title">土法防水水泥</div>
<div class="card-desc">石灰 + 炉渣 = 不怕水的古代水泥</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#基建改造</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🌉</span>
<div class="card-title">拱桥与承重结构</div>
<div class="card-desc">拱形承重原理，千年石桥不倒塌</div>
<div class="card-tags"><span class="tag">一月量产</span><span class="tag">#基建改造</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">⚙️</span>
<div class="card-title">水车与省力滑轮</div>
<div class="card-desc">水力自动、滑轮省力，古代版"机械化"</div>
<div class="card-tags"><span class="tag">当日~一月</span><span class="tag">#基建改造</span><span class="tag">#无电力</span></div>
</div>
</div>

### 算学

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🔢</span>
<div class="card-title">阿拉伯数字速算</div>
<div class="card-desc">竖式计算，比算筹快三倍</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#低成本</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">📐</span>
<div class="card-title">勾股测距测地</div>
<div class="card-desc">3-4-5 画直角，竹竿法测山高</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#基建改造</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">📒</span>
<div class="card-title">统计台账管理</div>
<div class="card-desc">人口粮食统计，制表管理一目了然</div>
<div class="card-tags"><span class="tag">当日落地</span><span class="tag">#低成本</span></div>
</div>
</div>

### 远工（多年布局）<a id="远工"></a>

<div class="knowledge-grid">
<div class="knowledge-card">
<span class="card-icon">🧫</span>
<div class="card-title">土法蒸馏酸碱</div>
<div class="card-desc">绿矾干馏得硫酸，硝石加热得硝酸</div>
<div class="card-tags"><span class="tag">数年</span><span class="tag">#高收益</span><span class="tag">#官府建功</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🔋</span>
<div class="card-title">简易铜锌电池</div>
<div class="card-desc">铜锌盐水，化学能变电能（仅科普演示）</div>
<div class="card-tags"><span class="tag">数年</span><span class="tag">#科普</span></div>
</div>
<div class="knowledge-card">
<span class="card-icon">🚂</span>
<div class="card-title">蒸汽机原理与瓶颈</div>
<div class="card-desc">热能转机械能，但古代造不出来</div>
<div class="card-tags"><span class="tag">数年</span><span class="tag">#基建改造</span><span class="tag">#不可行</span></div>
</div>
</div>

### ⚠️ 避坑指南 <a id="避坑"></a>

> 以下技术看似简单，实则隔着整个工业革命，**不要在这些技术上浪费时间**。

<div class="knowledge-grid">
<div class="knowledge-card" style="border-left: 4px solid #800080;">
<span class="card-icon">🚫</span>
<div class="card-title">电力芯片相关全部作废</div>
<div class="card-desc">发电机、电动机、电灯、无线电、芯片……全部需要现代工业体系支撑</div>
<div class="card-tags"><span class="difficulty-badge diff-impossible">永远不可行</span></div>
</div>
<div class="knowledge-card" style="border-left: 4px solid #800080;">
<span class="card-icon">🚫</span>
<div class="card-title">精密机械与高分子材料</div>
<div class="card-desc">精密机床、内燃机、塑料橡胶……缺少整个产业链</div>
<div class="card-tags"><span class="difficulty-badge diff-impossible">永远不可行</span></div>
</div>
<div class="knowledge-card" style="border-left: 4px solid #800080;">
<span class="card-icon">🚫</span>
<div class="card-title">现代社会体系无法落地</div>
<div class="card-desc">现代金融、法律、互联网体系……脱离经济基础就是空文</div>
<div class="card-tags"><span class="difficulty-badge diff-impossible">永远不可行</span></div>
</div>
</div>

---

## 📖 文档规范

每篇技术文档均包含以下章节：

1. **现代底层原理** — 用通俗语言解释科学逻辑
2. **古代实操完整步骤** — 纯人力、土设备可完成的步骤
3. **优势对比** — 与古代现有技术的差距
4. **局限性与短板** — 资源限制与风险提示
5. **拓展延伸** — 关联技术文档跳转

---

> 💡 本知识库所有内容仅供网文创作参考、历史技术研究与教育用途。部分技术（如黑火药）在现实中可能受到法律法规严格管制，请勿在实际生活中违规操作。
