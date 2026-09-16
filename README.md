# Linyi Sourcing Intel — 知识主库

> `Dameon · Linyi Sourcing` 项目的唯一知识主库（Single Source of Truth）。
> 建库日期：2026-09-16。

## 这个库是什么

临沂采购代理（Linyi Sourcing Agent）海外社媒项目的公共知识库：公开情报、脱敏供应链资源、内容骨架、发布表现记录。

**GitHub repo 是知识主库，不是客户 CRM，不是合同库，不是视频素材库。**

## 谁维护

- **ChatGPT**：总指挥、内容策略、人物定位、选题、脚本最终决策
- **WorkBuddy**：执行、公开数据调研、知识库维护、结构化录入
- **Claude**：阶段性读取 GitHub 内容，做方向复盘和第二意见

冲突时优先级：**GitHub 当前 main 分支内容 > Claude 项目知识 > AI 临时上下文**。任何 AI 不得另建"第二知识库"。

写库规范见 [AGENTS.md](AGENTS.md)，定位见 [positioning.md](positioning.md)。

## 各目录放什么

```text
linyi-sourcing-intel/
├── README.md            # 本文件
├── AGENTS.md            # AI 写库统一规范
├── positioning.md       # 当前锁定版定位
├── 01_intel/            # 公开情报（全部带来源链接）
│   ├── city-data.md         # 城市商贸物流官方数据 + 对外贸易/目标市场
│   ├── markets.md           # 专业市场 + 县区产业带
│   ├── buyer-research.md    # 海外买家痛点（Reddit 实采整理）
│   ├── competitors.md       # 海外对标账号数据库
│   └── logistics.md         # 出口物流路径 + 清关要点
├── 02_suppliers/        # 供应商与产品（脱敏）
│   ├── suppliers.md         # 供应商 ID 索引（schema）
│   └── products.md          # public_price 产品表（schema）
├── 03_content/          # 内容
│   ├── hooks.md             # Hook 句库
│   ├── backlog.md           # 视频 backlog
│   ├── media-index.md       # 素材索引（暂缓整理，见文件说明）
│   └── scripts/             # 最终脚本
└── 04_performance/
    └── videos.md            # 发布表现记录
```

## 哪些资料禁止进入

客户私人资料、供应商真实身份与联系人、成交底价、返点、账期、利润率、合同、PI、付款凭证、银行资料、任何 secret（key/token/password/cookie/私钥）。完整清单与判断标准见 [AGENTS.md](AGENTS.md) 第 1、3 节。

## 正常工作流程

```text
公开研究
→ 01_intel

真实供应商公开可用数据
→ 02_suppliers

情报 + 真实供应链资源
→ 03_content

发布
→ 04_performance

表现反馈
→ 下一轮选题与脚本
```

## 数据来源说明

本库初始情报由 WorkBuddy 于 2026-09-09 ~ 2026-09-15 完成 6 大板块调研（官方数据 / 市场产业带 / 出口结构 / Reddit 100 问 / 物流路径 / 24 账号库），原始采集文件归档于 WorkBuddy 工作区 `research/2026-09-09`、`research/2026-09-10`、`research/2026-09-15` 目录，作为本库的证据底稿，保持只读。

引用规则：所有数字回链原始来源；无法验证的不写成事实；实时运费一律"需货代实询"。
