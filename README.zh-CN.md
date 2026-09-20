# 美学工作室

![Aesthetic Atelier](demo/repo-hero-poster.jpg)

> High Aesthetic Image Expert · 1 个技能 + 2 个子技能  
> Matching Couple Avatar · Photo Style Transfer Poster · 克制、关系优先、留白

[English](README.md) | **简体中文**

**一个技能 —— High Aesthetic Image Expert —— 带两个子技能**，专注高审美图像创作。以 `SKILL.md` 操作手册的形式交付，并附带作为回归记忆的示例图集。

本包的表达基调是**正向锁定**：明确说出要保留和交付什么。只有当某种失败模式反复出现时，才使用强调式禁令。

```
aesthetic-atelier/
├── high-aesthetic-image-expert/SKILL.md      ← 技能本体
├── matching-couple-avatar/                   ← 子技能 1
│   ├── SKILL.md          薄入口 + 加载协议
│   ├── CORE.md           默认加载 —— 法则
│   ├── STUDY.md          按需 —— 实测协议
│   ├── ATLAS.md          按需 —— 失败图鉴 F1–F8
│   └── APPENDIX.md       按需 —— 模板与操作笔记
├── photo-style-transfer-poster/              ← 子技能 2
│   ├── SKILL.md          薄入口 + 加载协议
│   ├── CORE.md           默认加载 —— 法则
│   ├── ATLAS.md          按需 —— 失败图鉴 F1–F7
│   └── recipes/          九张配方卡，一次只开一张
└── demo/                                     ← 回归示例图集
    ├── MANIFEST.md         每张图的角色 —— 权威来源
    ├── avatar_demo/        情侣头像组（1L–4L）
    ├── poster_demo1/       风格迁移批次 A（原图 + 9 种风格 + 9 张画幅对齐）
    ├── poster_demo2/       风格迁移批次 B（原图 + 9 种风格 + 9 张画幅对齐）
    └── bear.jpg            通用任务示例
```

**快速跳转：** [技能构成](#技能构成) · [九种配方](#九种配方) · [示例图库](#示例图库) · [生成提示词](#生成提示词) · [安装](#安装) · [共同信条](#共同信条) · [许可证](#许可证)

---

## 技能构成

**High Aesthetic Image Expert** 是一位审美画图专家，也是**任何**图像需求的入口 —— 写实照片、插画、情绪图、海报、壁纸、概念图，或者只存在于文字里的场景。它执行一套固定的美学内核（克制、关系优先、色彩源于内容、装饰稀疏、留白即设计、先解构再重建、只交付成品），并在交付前强制执行一次自检。

两个子技能是**针对两类高频任务的专项特训**，而不是这个技能的能力边界：

- **Matching Couple Avatar（情侣头像）** 拿到用户的一张头像，**只画一张**新头像与之配对。这不是一次出两张图 —— 你提供的头像永远不会被重绘或修改，只补画缺失的那一半。生成由从原图实测的像素级锁定驱动（线条材质、五官配方、配色、背景），因此配对头像看起来出自同一位画师之手、但身份是全新的，并与原图构成**对子**式的互补关系，而不是镜像复制。
- **Photo Style Transfer Poster（风格迁移海报）** 把一张照片变成同一时刻、同一空间的一张完成稿 —— 是风格化重建，绝不是照片本身，也绝不是前后对比排版。两道硬锁把关：所有重要人物、动物和姿态关键道具必须完整留在画面内；原图的空间结构必须保持不变。内置九种版画 / 插画配方。

除此之外的一切 —— 其他任何题材、风格或需求 —— 都由技能本体直接处理。

### 运行时加载

手册是**分层**的，所以冷启动不会把 80KB 全灌进上下文。每个子技能的 `SKILL.md` 都写了自己的协议：

- **始终加载：** 该子技能的 `SKILL.md` + `CORE.md` —— 目标、硬锁、流程、自检。
- **按需 —— `ATLAS.md`：** 只在翻车或用户抱怨之后打开，用来对照 F 码。
- **按需 —— `STUDY.md` / `APPENDIX.md`：** 只在 CORE 的锁定不足以写出实测数值时打开。
- **一次一张 —— `recipes/*.md`：** 绝不预加载九张卡。

父技能路由到子技能时，只加载它的 `SKILL.md` + `CORE.md`，不加载整本手册。

---

## 九种配方

| # | 配方 | 是什么 |
|---|---|---|
| 1 | **RISO Editorial** | 孔版套色印刷，手绘线条、套印错位、暖色纸张颗粒。 |
| 2 | **Old Newsprint** | 泛黄旧报纸文化副刊，网点主图 + 多栏编辑版式。 |
| 3 | **Paper Theatre** | 分层剪纸立体剧场，可见铆钉与纸层景深。 |
| 4 | **Pressed Flower** | 植物标本拼贴，用干花瓣与叶片重建主体剪影。 |
| 5 | **Travel Journal Sketch** | 钢笔 + 彩铅速写，锁死同一瞬间与空间关系。 |
| 6 | **Retro Silkscreen** | 高对比粗网点丝网印，粗体字与颗粒色块。 |
| 7 | **JP B&W Line** | 安静的日系黑白线稿生活方式插画，大量留白。 |
| 8 | **Naïve Doodle** | 主体画得小但完整，大面积刻意留白。 |
| 9 | **Photo→Ink Sketch** | 暖色纹理纸上的松散黑白墨线，同一主体。 |

**氛围 → 配方**，用于只说了感觉、没指定风格的需求：

| 氛围 | 首选 | 也可考虑 |
|---|---|---|
| 怀旧、复古、胶片、旧杂志 | Photo→Ink / Old Newsprint / Retro Silkscreen | 旅行题材则用 Travel Journal |
| 电影海报、电影感 | Photo→Ink / Retro Silkscreen | — |
| 文艺、独立杂志、展览海报 | RISO Editorial | 极简大留白则用 Naïve Doodle |
| 报纸、副刊、知性、编辑感 | Old Newsprint | — |
| 手工、纸艺、童话剧场、立体书 | Paper Theatre | — |
| 压花、标本、植物、节日温柔 | Pressed Flower | 情侣 / 节日 / 植物题材 |
| 旅行、速写、日记、城市写生 | Travel Journal Sketch | 更安静的黑白则用 JP B&W Line |
| 先锋、丝网、实验印刷 | Retro Silkscreen | 想更柔和则用 RISO |
| 治愈、日系、黑白线稿、露营街头 | JP B&W Line | 想更俏皮则用 Naïve Doodle |
| 涂鸦、稚拙、大留白、少即是多 | Naïve Doodle | 仍想要印刷色彩则用 RISO |

没有给氛围时，由照片内容决定：建筑或街景 → Travel Journal；柔光人像 → Photo→Ink；情侣、节日或花卉 → Pressed Flower；戏剧化布景 → Paper Theatre；强烈图形感面孔 → Retro Silkscreen；安静日常 → JP B&W Line；纪实城市记忆 → Old Newsprint；稀疏线条配聪明排版 → Naïve Doodle。

---

## 示例图库

两个子技能都把这些示例当作**回归测试集** —— 质量下滑时就重新打开对照。输入到输出的完整示例见 [生成提示词](#生成提示词)。

**回归角色：** 只有 `gold`（以及作为锁定起点的 `source`）才是正例。`working-attempt` 和 `fail-example` 只用于**找差距** —— 绝不能当成交付样板照抄。每张图的权威定义见 [`demo/MANIFEST.md`](demo/MANIFEST.md)。

### 情侣头像 — `demo/avatar_demo/`

> **一张进，一张出。** 这不是一次出两张图。你交出来的头像永远不会被重绘或修改 —— 技能只画一张新头像，摆在它的对面。常见情况是你手上只有一半：自己的头像，或者喜欢的人（暗恋对象）的照片，另一半需要画出来配对。

`L`/`R` 是**组号，不是"画面左/右"** —— 朝向以像素为准。

| 组 | 原图（`nL`）— **`source`** | 已认可的配对（`nR`）— **`gold`** | 生成的配对头像（`nL_gen`）— **`working-attempt`** |
|:---:|:---:|:---:|:---:|
| 1 | <img src="demo/avatar_demo/1L.jpeg" width="200"> | <img src="demo/avatar_demo/1R.jpeg" width="200"> | <img src="demo/avatar_demo/1L_gen.jpeg" width="200"> |
| 2 | <img src="demo/avatar_demo/2L.jpeg" width="200"> | <img src="demo/avatar_demo/2R.jpeg" width="200"> | <img src="demo/avatar_demo/2L_gen.jpeg" width="200"> |
| 3 | <img src="demo/avatar_demo/3L.jpg" width="200"> | <img src="demo/avatar_demo/3R.jpg" width="200"> | <img src="demo/avatar_demo/3L_gen.jpg" width="200"> |
| 4 | <img src="demo/avatar_demo/4L.jpg" width="200"> | <img src="demo/avatar_demo/4R.jpg" width="200"> | <img src="demo/avatar_demo/4L_gen.jpg" width="200"> |

研习方法：打开 `nL`，锁定朝向、比例、线条、五官配方、背景与色偏；打开 `nR` 作为配对语法的范例；打开 `nL_gen` 作为一次实际尝试；列出差距，再用更紧的锁定重新生成。

**失败图鉴 F1–F8：** 标签驱动的素材库画风 · 空间塌陷（特写放大 / 不安全的方形裁切）· 背景丢失 · 用镜像复制冒充对子 · 线条方言错误（沉默的杀手）· 只调代理指标 · 修补失败底稿而不重画 · 服装明暗对子污染整幅画面。

### 风格迁移批次 A — `demo/poster_demo1/`

海岸 / 街道记忆批次。用于练习轴线、景深与完整行人。

> **画幅说明：** 本节的 `style-01`…`style-09` 是 **1280×720（生成器原生，16:9）**，与各自 `raw.jpg` 的画幅不一致 —— 批次 A 的原图≈4:3（1706×1279），批次 B≈1.51（1024×677）。这些图用于**配方方言**对照；对外交付时须按技能的 pad 规程对齐源图画幅（`CORE.md §6c`）。`*_matched.jpg` 是同一张图 letterbox 到原图画幅的版本，做空间对照请用它们。

**原图** — `demo/poster_demo1/raw.jpg`

<img src="demo/poster_demo1/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-01-riso.jpg" width="240"> | <img src="demo/poster_demo1/style-02-newsprint.jpg" width="240"> | <img src="demo/poster_demo1/style-03-paper-theatre.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-04-pressed-flower.jpg" width="240"> | <img src="demo/poster_demo1/style-05-travel-sketch.jpg" width="240"> | <img src="demo/poster_demo1/style-06-silkscreen.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo1/style-07-jp-line.jpg" width="240"> | <img src="demo/poster_demo1/style-08-naive-doodle.jpg" width="240"> | <img src="demo/poster_demo1/style-09-ink-sketch.jpg" width="240"> |

回归：先对照 `raw.jpg` 与 `style-05` / `style-09`（空间要求最高），再看大留白配方的裁切风险。**⑧ Naïve Doodle** 在这里是 `working-attempt`（F6 —— 行人被简化），不算空间合格。

### 风格迁移批次 B — `demo/poster_demo2/`

山谷场景，**女性主体居中、背对镜头**，望向山谷 —— 是"完整人形 + 山谷景深 + 同一地点辨识度"的强测试。

> **画幅说明：** 本节的 `style-01`…`style-09` 是 **1280×720（生成器原生，16:9）**，与各自 `raw.jpg` 的画幅不一致 —— 批次 A 的原图≈4:3（1706×1279），批次 B≈1.51（1024×677）。这些图用于**配方方言**对照；对外交付时须按技能的 pad 规程对齐源图画幅（`CORE.md §6c`）。`*_matched.jpg` 是同一张图 letterbox 到原图画幅的版本，做空间对照请用它们。

**原图** — `demo/poster_demo2/raw.jpg`

<img src="demo/poster_demo2/raw.jpg" width="420">

| ① RISO Editorial | ② Old Newsprint | ③ Paper Theatre |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-01-riso.jpg" width="240"> | <img src="demo/poster_demo2/style-02-newsprint.jpg" width="240"> | <img src="demo/poster_demo2/style-03-paper-theatre.jpg" width="240"> |

| ④ Pressed Flower | ⑤ Travel Journal Sketch | ⑥ Retro Silkscreen |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-04-pressed-flower.jpg" width="240"> | <img src="demo/poster_demo2/style-05-travel-sketch.jpg" width="240"> | <img src="demo/poster_demo2/style-06-silkscreen.jpg" width="240"> |

| ⑦ JP B&W Line | ⑧ Naïve Doodle | ⑨ Photo→Ink Sketch |
|:---:|:---:|:---:|
| <img src="demo/poster_demo2/style-07-jp-line.jpg" width="240"> | <img src="demo/poster_demo2/style-08-naive-doodle.jpg" width="240"> | <img src="demo/poster_demo2/style-09-ink-sketch.jpg" width="240"> |

回归：确认背身剪影完整（与原图一样从头顶到衣摆），且九种风格的谷底景深保持不变。**⑧ Naïve Doodle** 在这里是 `fail-example`（F2 —— 秋冬分屏改写了地点身份），绝不能当作空间正例。

**失败图鉴 F1–F7：** 留白后人物不完整 · 元素库式空间重写 · 成片里出现原照片或对比排版 · 强行套错画幅 · 字体或裁切线切到人体 · 清理杂物时删掉了人 · 只调代理指标。

配方 ⑤ 旅行速写、⑦ 日系线稿、⑨ 墨线对**空间**最严格；大留白的 ① 与 ⑧ 最容易在**裁切**上翻车。当用户说结果"不尊重这张照片"时，先查 ⑤⑦⑨，再查 ①⑧ 的裁切风险。

---

## 生成提示词

真实交互长什么样。下面三个示例都用同一套结构：**Prompt**，然后**输入**，然后**输出**。

### 通用需求 —— 根据小说场景作画

**Prompt**

> 以下是一段《挪威的森林》中的文字，我希望根据描绘生成一个尽量唯美、浪漫、文艺的高分辨率图像：
>
> "最最喜欢你，绿子。"
> "什么程度？"
> "像喜欢春天的熊一样。"
> "春天的熊？"绿子再次扬起脸，"什么春天的熊？"
> "春天的原野里，你正一个人走着，对面走来一只可爱的小熊，浑身的毛活像天鹅绒，眼睛圆鼓鼓的。它这么对你说道：'你好，小姐，和我一块打滚玩好么？'接着你就和小熊抱在一起，顺着长满三叶草的山坡咕噜咕噜滚下去，整整玩了一大天。你说棒不棒？"
> "太棒了。"
> "我就这么喜欢你。"

**输入** — 上面那段文字（有删节）；没有参考图

**输出** — `demo/bear.jpg`

<img src="demo/bear.jpg" width="520">

### 情侣头像

**Prompt**

> 给你一张头像，我想要生成对应的情侣头像。

| **输入** — `demo/avatar_demo/3L.jpg` | **输出** — `demo/avatar_demo/3L_gen.jpg` |
|:---:|:---:|
| <img src="demo/avatar_demo/3L.jpg" width="240"> | <img src="demo/avatar_demo/3L_gen.jpg" width="240"> |

原文件保持不变。输出的是一张新头像，同一支笔、朝向相反，两张摆在一起读得出是一对。

### 风格迁移 —— 印花标本（Pressed Flower）

**Prompt**

> 给你一张照片，我想要生成一张印花风格的文艺海报。

| **输入** — `demo/poster_demo2/raw.jpg` | **输出** — `demo/poster_demo2/style-04-pressed-flower.jpg` |
|:---:|:---:|
| <img src="demo/poster_demo2/raw.jpg" width="240"> | <img src="demo/poster_demo2/style-04-pressed-flower.jpg" width="240"> |

同一张照片、同一时刻、同一空间：主体保持完整、布局原地不动，只有媒介变了。把风格名换成上表九种配方中的任意一个即可。

---

## 安装

> **TL;DR —— 直接对你的 agent 说 *"install this repo"* 就行。** 它会克隆本包并把技能软链到自己的 skills 目录；Claude Code、Cursor、Codex 各自知道自己的目录在哪。下面是可以手动控制文件落点的完整做法。

每个技能目录都是自包含的：目录名就是技能 slug，`SKILL.md` 里的 YAML frontmatter（`name`、`description`）用于被发现和路由。格式遵循 [Agent Skills](https://agentskills.io) 标准，所以同一批目录可以跨工具使用。

### 1. 克隆本包

```bash
git clone <this-repo-url> ~/aesthetic-atelier
cd ~/aesthetic-atelier
```

### 2. 把技能链进你的工具

**Claude Code** —— 个人级（所有项目）或项目级：

```bash
SKILLS=~/.claude/skills          # 个人级
# SKILLS=.claude/skills          # 项目级，可提交给团队共享
mkdir -p "$SKILLS"
for s in high-aesthetic-image-expert matching-couple-avatar photo-style-transfer-poster; do
  ln -sfn "$PWD/$s" "$SKILLS/$s"
done
```

Claude Code 要求 `<skill-name>/SKILL.md` 直接位于 skills 根目录下，之后可用 `/matching-couple-avatar` 等方式调用。不用软链的话，把每个目录复制进 `~/.claude/skills/` 也一样。

**Cursor** —— Cursor 会递归扫描 skills 根目录，并以包含 `SKILL.md` 的目录名作为技能名，所以整包一个软链就够：

```bash
ln -sfn ~/aesthetic-atelier ~/.cursor/skills/aesthetic-atelier
# 或项目级：
# ln -sfn ~/aesthetic-atelier .cursor/skills/aesthetic-atelier
```

Cursor 会读取 `.cursor/skills/`、`.agents/skills/` 及其 `~/` 全局对应目录，同时也兼容读取 `.claude/skills/` 和 `.codex/skills/`。你也可以用内置的 `/create-skill` 创建自己的技能。

**Codex** —— 用户级，或仓库内的 `.agents/skills/`：

```bash
SKILLS=~/.agents/skills          # 用户级
mkdir -p "$SKILLS"
for s in high-aesthetic-image-expert matching-couple-avatar photo-style-transfer-poster; do
  ln -sfn "$PWD/$s" "$SKILLS/$s"
done
```

Codex 会读取 `$CWD/.agents/skills`、`$REPO_ROOT/.agents/skills`、`$HOME/.agents/skills` 与 `/etc/codex/skills`，并支持软链的技能目录。可以在 `~/.codex/config.toml` 里用 `[[skills.config]]` 临时禁用某个技能而不删除它。

**其他任何支持 Agent Skills 的工具** —— 项目内的 `.agents/skills/` 或全局的 `~/.agents/skills/` 是 Codex 与 Cursor 共同读取的通用约定。

| 工具 | skills 根目录 | 发现方式 |
|---|---|---|
| Claude Code | `~/.claude/skills/` · `.claude/skills/` | `<skill-name>/SKILL.md`；用 `/skill-name` 调用 |
| Cursor | `~/.cursor/skills/` · `.cursor/skills/` · `.agents/skills/` | 递归 —— 支持嵌套分类目录 |
| Codex | `~/.agents/skills/` · `.agents/skills/` · `/etc/codex/skills` | 支持软链目录 |
| 通用 | `.agents/skills/` | Agent Skills 标准 |

### 3. 让示例图集可用（可选）

两个子技能都把示例标注为"有则可读"。它们以包内相对路径引用，例如 `aesthetic-atelier/demo/avatar_demo/`。由于示例目录与技能目录平级而非嵌套，建议告诉你的 agent 本包在哪 —— 比如在 `AGENTS.md` / `CLAUDE.md` 里加一行：

```markdown
High aesthetic image skills pack is cloned at ~/aesthetic-atelier.
Demo regression sets: ~/aesthetic-atelier/demo/{avatar_demo,poster_demo1,poster_demo2}
```

会递归扫描的工具（Cursor）也可以直接用上面那条整包软链，这样文档里写的路径就原样有效。

### 4. 验证

```bash
ls -l ~/.claude/skills/ | grep -E 'aesthetic|couple|poster'
head -12 ~/.claude/skills/matching-couple-avatar/SKILL.md
```

然后随便给 agent 一个图像需求，确认它加载了对应技能 —— 自动选中靠的就是 `description` 字段。

**Matching Couple Avatar** 的 description 同时带有中文触发词，所以用中文提"情侣头像"会直接命中这个子技能。本包其余技能的描述均为纯英文。

---

## 共同信条

两个子技能都建立在同一套固定美学内核之上，各自再叠加自己的法则。压缩成几句：

- **像素级锁定主导，标签处于从属地位。** 类型标签是概括，不是锁定。
- **主体与空间是第一道验收关** —— 配色和颗粒最后再说。
- **实测，别凭感觉** —— 把人脸占比、亮度、画幅、轴线位置写进需求里。
- **在更好的锁定下重画**，而不是修补一张失败的底稿。
- **先指出出问题的那条轴**（线条 / 五官 / 空间 / 背景 / 对子），再动手改。
- **用户一旦定稿就停手** —— 存为 `*_gen`，不再反复重生成。
- **推荐配方用名字，不用编号。**
- **把示例图集当作回归记忆。**

---

## 许可证

基于 [MIT License](LICENSE) 发布。Copyright (c) 2026 zijianwang。
