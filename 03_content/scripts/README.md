# scripts/README.md — 内容工作流规范 / Content Production Workflow

> 本目录存放 ChatGPT 最终确认的视频脚本。每条视频一个文件，命名：`V001-slug.md`。
> WorkBuddy 不自行撰写定稿脚本，只在 ChatGPT 明确批准后录入。
>
> This directory stores final video scripts approved by ChatGPT.
> One file per video, named `V001-slug.md`.
> WorkBuddy does not independently create final scripts; it records them only after approval.

**本文件是内容生产流程的唯一规范来源 / Single source of truth for the content workflow.**
以下四类规则统一写在本文件，不再分散：

1. 内容状态定义 / Content status definitions
2. 定稿脚本必备结构 / Required structure for approved scripts
3. 内容重复度检查 / Content overlap check
4. 标准内容工作流 / Standard content workflow

**文件层级 / File layers**

| 文件 | 职责 / Responsibility |
|---|---|
| `AGENTS.md` | 仓库宪法 — 全库通用规则与安全边界 |
| `positioning.md` | 品牌战略 — 定位、平台、决策记录 |
| `03_content/backlog.md` | 未来拍什么 — 选题与状态 |
| `03_content/scripts/README.md` | 内容怎么生产、怎么查重、怎么入库 —— **本文件** |
| `03_content/scripts/Vxxx.md` | 每条最终内容 |
| `04_performance/videos.md` | 发出去以后表现怎么样 |

---

## 1. Content Status Definitions / 内容状态定义

以后所有视频必须使用以下状态之一。Every video must use one of these statuses.

| 状态 | 中文 | English |
|---|---|---|
| `idea` | 只有想法，还没排期 | Idea only |
| `planned` | 方向已经确定，但脚本尚未最终批准 | Direction confirmed, final script not yet approved |
| `draft` | ChatGPT 已经写脚本，但 Damon 尚未最终确认 | Script drafted by ChatGPT but not yet approved by Damon |
| `approved` | Damon + ChatGPT 已确认，可以执行拍摄 | Approved by Damon + ChatGPT, ready for production |
| `shot` | 已经拍摄，尚未正式发布 | Filmed but not published |
| `published` | 已经发布 | Published |
| `retired` | 因为方向变化或内容重复，不再执行 | No longer active due to strategy change or duplication |

> 本状态体系取代旧标签（`needs-script` / `needs-market` / `needs-market-data` / `needs-supplier` / `waiting-real-case` / `waiting-real-qc-case`）。旧标签不再使用。

---

## 2. Required Structure for Approved Scripts / 定稿脚本必备结构

以后进入本目录的正式脚本**至少**包含以下 11 段。
目的：做到 100、200 条视频以后，仍可回溯 —— 拍过什么、说过什么、用过什么数据、用过什么 Hook、下一次怎么避免重复。

| # | 段 / Section | 内容 |
|---|---|---|
| 1 | Metadata | `video_id` / `status` / `title_en` / `title_cn` / `pillar` / `category` / `approved_date` / `planned_location` / `delivery_mode` |
| 2 | Core Promise / 核心承诺 | 这条视频承诺让观众获得什么 |
| 3 | Hook | 前 3–5 秒，逐字保留 |
| 4 | Full Script EN | 英文正文，按时间轴逐段，逐字保留 |
| 5 | 中文理解 | 与英文逐段对应的中文理解 |
| 6 | Visual Plan | 逐段画面与屏幕大字 |
| 7 | Facts / Products Used | 用到的数字、SKU、`public_price`、MOQ、工艺点 |
| 8 | CTA | 允许三种类型：`Direct CTA` / `Soft CTA` / `None — intentional`。必须写明类型；`None — intentional` 须写明理由 |
| 9 | Related Videos | 与其它视频的承接关系 |
| 10 | Content Memory | Main Question / Core Facts Already Used / Core Visuals Already Used |
| 11 | Do Not Repeat | 以后不得再作为整条视频主要价值的角度 |

**CTA 类型 / CTA types**：`Direct CTA`（明确行动引导）｜`Soft CTA`（软引导）｜`None — intentional`（刻意不设行动 CTA，须写明理由）。

**WorkBuddy 不得为了满足模板而强行补 CTA。**

> Metadata 不要做复杂。Do not add unnecessary metadata fields.

---

## 3. Content Overlap Check / 内容重复度检查

以后 ChatGPT 准备一条新视频之前，WorkBuddy 根据以下三类文件进行一次**机械式**重复度检查：

- `03_content/scripts/`（已入库定稿脚本）
- `03_content/backlog.md`（已规划选题）
- `03_content/hooks.md`（已用 Hook 公式）

检查五个维度 / Five dimensions:

| # | 维度 | 判据 |
|---|---|---|
| 1 | Topic / 主题 | 是不是同一个**市场 / 工厂 / 产品 / 品类** |
| 2 | Core Question / 核心问题 | 观众看完后得到的主要答案是否一样（"有什么？" / "多少钱？" / "怎么生产？" / "为什么价格不同？" 属于不同问题） |
| 3 | Information / 信息载荷 | 是否重复使用相同**数据 / SKU / `public_price` / MOQ / 工艺知识 / QC 点** |
| 4 | Hook / 开场承诺 | 前 3–5 秒是否在承诺基本相同的内容 |
| 5 | Visual Structure / 画面结构 | 主体画面是否再次主要依赖**同一个展厅 / 同一条生产线 / 同一组货架 / 同一种流水线镜头** |

---

## 4. Overlap Scoring / 重复度评分

每个维度打分 / Per-dimension score:

- `0` = 基本不同 / distinct
- `1` = 部分重合 / partial overlap
- `2` = 高度重合 / substantial overlap

总分 0–10 / Total 0–10:

| 分数 | 判定 | 处理 |
|---|---|---|
| 0–3 | `LOW OVERLAP`（重复度低） | 可以进入脚本策划 |
| 4–6 | `MEDIUM OVERLAP`（存在明显重合） | WorkBuddy **不自行否决**，必须告诉 ChatGPT：重复在哪里、哪些部分需要换角度 |
| 7–10 | `HIGH OVERLAP`（与已有内容高度相似） | WorkBuddy **不自行删除选题**，必须提交 ChatGPT 决策：是否取消 / 是否换核心问题 / 是否延后发布 / 是否重新设计 Hook、信息、画面 |

> WorkBuddy 只负责**记忆和查重**；选题取舍与角度创新由 ChatGPT 判断。

---

## 5. Same Category Does Not Mean Duplicate / 同品类不等于重复

同一品类（一次性食品包装）下的四条选题 —— 涉及资源：澳强家超级展厅 / 碗汇 / 嘉澳 / 泰合：

| 视频 | 核心问题 / Core question | 类型 |
|---|---|---|
| `V003` | 这里能采购什么？ | Showroom / sourcing range |
| `V006` | 产品怎么生产？（吸塑） | Manufacturing |
| `V009` | 为什么两个产品价格不同？ | Price differences |
| `V012` | 注塑生产到底是什么样？ | Injection molding |

虽然都涉及一次性食品包装，但：**核心问题不同 = 内容可以成立。**

Same category does not automatically mean duplicate content.

---

## 6. Standard Content Workflow / 标准内容工作流

```text
Damon provides real-world resources
↓
WorkBuddy checks existing scripts/backlog for overlap
↓
ChatGPT decides topic and angle
↓
ChatGPT writes bilingual script
↓
Damon approves
↓
WorkBuddy archives approved script in GitHub
↓
Damon films
↓
Video is published
↓
WorkBuddy records performance data
↓
ChatGPT reviews results and adjusts strategy
```

中文：

```text
Damon 提供真实资源
↓
WorkBuddy 查历史内容和重复度
↓
ChatGPT 决定选题和角度
↓
ChatGPT 写中英双语脚本
↓
Damon 最终确认
↓
WorkBuddy 将 approved 脚本入 GitHub
↓
Damon 拍摄
↓
发布
↓
WorkBuddy 回填表现数据
↓
ChatGPT 复盘并调整下一阶段方向
```

> 简记：**查重 → 写 → 批准 → 入库 / overlap check → script → approval → archive**
