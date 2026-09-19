# AGENTS.md — AI 写库统一规范

> 本文件约束所有向本知识库写入内容的 AI（ChatGPT / WorkBuddy / Claude）。
> 冲突时优先级：**GitHub 当前 main 分支内容 > Claude 项目知识 > AI 临时上下文**。
> 任何 AI 不得另建"第二知识库"。

---

## 1. 绝对禁止进入 Git 的内容

- 客户真实姓名、公司名、手机号、微信、邮箱等私人业务资料
- 未授权公开的供应商真实身份和联系人
- 成交底价
- 返点
- 账期
- 特殊采购条件
- 利润率
- 合同
- PI
- 付款凭证
- 银行资料
- API key / token / password / cookie / SSH or private key

**发现疑似敏感内容：停止写入并报告。不得自行猜测脱敏后继续。**

## 2. 供应商 ID

格式：`SUP-{CATEGORY}-{NNN}`，例如 `SUP-PP-001`。

**默认规则**：Git 中只记录脱敏供应商信息，真实身份由 Damon 在库外保存。

**例外（2026-09-18 增补）**：如果 Damon 已明确确认某供应商名称可以公开，则允许在 Git 中记录该供应商的 `public_name`，但必须同时满足：

- `public_identity_allowed = yes`
- 名称由 Damon 明确提供或确认
- 不记录联系人
- 不记录手机号 / 微信 / 邮箱
- 不记录 internal_cost / 返点 / 账期 / 利润
- 不记录合同 / PI / 支付资料

未明确授权公开的供应商仍只能使用 `supplier_id`。

English:

Supplier identities remain private by default.

A supplier's public name may be stored only when Damon has explicitly confirmed that the identity is public and `public_identity_allowed = yes`.

Contacts and sensitive commercial information remain prohibited.

## 3. 两种价格严格区分

### public_price（允许进入 Git）

必须同时满足：

- 真实采集价格
- 用户确认可以公开
- 带采集日期
- 带币种
- 带贸易条件
- 带 MOQ
- 带 supplier_id
- `publishable = yes`

示例：

```markdown
| sku | product | supplier_id | public_price | moq | terms | observed | publishable | note |
|---|---|---|---:|---:|---|---|---|---|
| PP-BOX-750 | PP food container 750ml | SUP-PP-001 | $0.026 | 100000 | EXW | 2026-09-20 | yes | |
```

正式 schema 统一为 `sku` / `product` / `supplier_id` / `public_price` / `moq` / `terms` / `observed` / `publishable` / `note`（与 `02_suppliers/products.md` 一致）。**不得引入第二个价格字段。**

### internal_cost（绝对禁止进入 Git）

包括：成交底价、返点、账期、特殊报价、利润率等。

判断标准：**这个数字能不能直接在公开海外视频里说？不能，就不能进知识库。**

## 4. 官方数据

任何进入 `01_intel/` 的数字必须保留：

- 数字
- 统计期间
- 来源机构
- 来源标题
- 来源链接
- 来源发布日期（能获得则写）
- 本库记录日期

无法验证的数字不要写成事实。

## 5. 日期

全部使用 `YYYY-MM-DD`。

## 6. 修改规则

不要为了改一条数据重写整个文件。数据变化时保留更新痕迹，例如：

`MOQ 50000（原 100000；2026-10-01 更新）`

## 7. Commit Message

禁止 `update` / `fix` / `new` 这类无意义 message。

使用类似：

- `docs: import verified Linyi trade research`
- `content: add initial launch-video backlog`

## 8. 其他

- 单文件超过约 500 行再讨论拆分；目前不提前设计复杂子目录。
- 本 repo 只保存 Markdown / CSV / 小型知识文件；禁止 Git LFS；不保存视频。
- 禁止把本库当客户 CRM、合同库、视频素材库使用。
