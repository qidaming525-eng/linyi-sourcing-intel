# scripts/README.md — 内容工作流规范 / Content Production Workflow

> 本目录存放 ChatGPT 最终确认的视频脚本。每条视频一个文件，命名：`V001-slug.md`。
> WorkBuddy 不自行撰写定稿脚本，只在 ChatGPT 明确批准后录入。
>
> This directory stores final video scripts approved by ChatGPT.
> One file per video, named `V001-slug.md`.
> WorkBuddy does not independently create final scripts; it records them only after approval.

**本文件是内容生产流程的唯一规范来源 / Single source of truth for the content workflow.**

---

## 1. Content Status Definitions / 内容状态定义

| 状态 | 中文 | English |
|---|---|---|
| `idea` | 只有想法，还没排期 | Idea only |
| `planned` | 方向已经确定，但脚本尚未最终批准 | Direction confirmed, final script not yet approved |
| `draft` | ChatGPT 已经写脚本，但 Damon 尚未最终确认 | Script drafted by ChatGPT but not yet approved by Damon |
| `approved` | Damon + ChatGPT 已确认，可以执行拍摄 | Approved by Damon + ChatGPT, ready for production |
| `shot` | 已经拍摄，尚未正式发布 | Filmed but not published |
| `published` | 已经发布 | Published |
| `retired` | 因为方向变化或内容重复，不再执行 | No longer active due to strategy change or duplication |

---

## 2. Full Production Package / 每一期完整交付标准

从 2026-09-20 起，**一条视频只有同时具备“内容 + 拍摄 + 发布”三层信息，才算完整交付。**

任何 `approved` 脚本至少包含以下 **16 段**：

| # | Section | 必须包含 |
|---|---|---|
| 1 | Metadata | `video_id` / `status` / `title_en` / `title_cn` / `pillar` / `category` / `approved_date` / `planned_location` / `delivery_mode` |
| 2 | Core Promise | 观众看完获得什么 |
| 3 | Hook | 前 3–5 秒逐字稿 |
| 4 | Full Script EN | 英文逐字稿 + timecode + delivery |
| 5 | 中文理解 | 与英文逐段对应 |
| 6 | Visual Plan | 每段画面、动作、On-screen text |
| 7 | Facts / Products Used | 数据、SKU、价格、MOQ、工艺等 |
| 8 | CTA | `Direct CTA` / `Soft CTA` / `None — intentional` |
| 9 | Related Videos | 前后承接关系 |
| 10 | Content Memory | 主问题、已用事实、已用核心画面 |
| 11 | Do Not Repeat | 后续不得重复的主要价值 |
| 12 | Titles & Cover | 主标题、备用标题、封面大字 |
| 13 | Shot-by-Shot Board | **逐镜头写清 Damon 真人 / B-roll / VO / Sync sound**，以及具体动作 |
| 14 | Publishing Caption | 英文主发布文案 + 中文理解；必要时给平台差异版 |
| 15 | Hashtags | 固定品牌标签 + 当期品类标签 |
| 16 | Shoot & Edit Checklist | 到现场必拍、收音、字幕、价格/隐私遮挡、剪辑节奏、素材禁区 |

### Delivery 标准词汇

每个镜头必须至少标一种：

- `ON-CAMERA` — Damon 真人直接口播
- `B-ROLL + VO` — 画面为产品/市场/工厂，后期英文旁白
- `B-ROLL + NAT SOUND` — B-roll 保留现场声
- `ON-CAMERA ACTION` — Damon 不一定说话，但本人需要出现在画面执行动作
- `TEXT-ONLY INSERT` — 只承担信息强调，不作为主体镜头

### Hashtag 固定基础组

除非某个平台规则变化或数据复盘要求调整，Damon 内容优先保留以下核心标签：

`#Linyi #LinyiSourcing #BuyAgent #ChinaSourcing #SourcingAgent`

每期再加 1–2 个**强相关品类标签**，例如：

- 一次性食品包装：`#FoodPackaging #WholesaleChina`
- 奶茶设备：`#BubbleTeaEquipment`
- 咖啡：`#CoffeeEquipment`
- 商厨：`#CommercialKitchen`

> Hashtag 不含空格，因此使用 `#LinyiSourcing`，不是 `#Linyi Sourcing`；使用 `#BuyAgent`，不是 `#Buy Agent`。

### 完整交付判定

如果只有逐字稿而缺少分镜、真人/B-roll 标记、封面、Caption 或 Hashtags，状态不得视为“production-ready”。

---

## 3. Content Overlap Check / 内容重复度检查

新视频进入脚本前，由 WorkBuddy 根据：

- `03_content/scripts/`
- `03_content/backlog.md`
- `03_content/hooks.md`

检查五个维度：Topic / Core Question / Information / Hook / Visual Structure。
每维 0–2，总分 0–10：

- 0–3：LOW OVERLAP
- 4–6：MEDIUM OVERLAP → 提交 ChatGPT 调整角度
- 7–10：HIGH OVERLAP → 提交 ChatGPT 决定取消 / 改问题 / 延后 / 重做

WorkBuddy 只负责记忆和查重；内容取舍由 Damon + ChatGPT 决定。

---

## 4. Same Category Does Not Mean Duplicate / 同品类不等于重复

同一次性食品包装可以存在不同问题：

| 视频 | 核心问题 | 类型 |
|---|---|---|
| V003 | 一站式展厅 + 三家自有工厂模式是什么？ | Showroom / sourcing model |
| V005 | 真实整箱价格与 MOQ 是多少？ | Price / MOQ / warehouse |
| V006 | 红白餐碗怎么生产？ | Manufacturing |
| V009 | 为什么相似产品价格不同？ | Price differences |
| V012 | 注塑餐盒如何生产？ | Injection molding |

核心问题不同，内容可以成立。

---

## 5. Standard Content Workflow / 标准内容工作流

```text
Damon provides real-world resources
↓
WorkBuddy checks overlap
↓
ChatGPT decides topic and angle
↓
ChatGPT writes FULL production package
(script + storyboard + delivery + cover + caption + hashtags + checklist)
↓
Damon approves
↓
Approved package archived in GitHub
↓
Damon films
↓
Publish
↓
WorkBuddy records performance
↓
ChatGPT reviews and adjusts
```

简记：**查重 → 完整拍摄包 → Damon 批准 → 入库 → 拍摄 → 发布 → 复盘。**
