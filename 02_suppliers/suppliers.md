# 供应商索引

> 规则见 AGENTS.md §2：**默认脱敏**；`public_name` 仅在 Damon 明确确认可公开、且 `public_identity_allowed = yes` 时填写。
> 联系人、手机号 / 微信 / 邮箱、成交底价、返点、账期、利润率、合同 / PI / 支付资料一律禁止入库。
> 供应商 ID 格式：`SUP-{CATEGORY}-{NNN}`。没有 Damon 提供并确认的数据之前，不填任何行。

| supplier_id | public_name | category | district | type | factory | shootable | public_identity_allowed | verified | note |
|---|---|---|---|---|---|---|---|---|---|
| SUP-PACK-001 | 澳强家 | disposable-food-packaging | | factory-backed-showroom | yes | yes | yes | Damon-confirmed | Damon-confirmed on 2026-09-20: Aoqiangjia operates a one-stop disposable-food-packaging showroom backed by **three owned factories**, with the three factories focusing on different product lines. This supports a factory-and-trade integrated / front-showroom-back-factory model. Do not imply that all products come from one production line or one single factory. The ownership mapping between these three factories and other supplier IDs in this repo is not yet explicitly confirmed; do not infer it. |
| SUP-PACK-002 | 碗汇 | disposable-food-packaging | | factory | yes | yes | yes | Damon-confirmed | Damon-provided: mainly thermoformed blue-and-white and red-and-white bowls. Do not publish "mid-to-high-end" positioning until separately confirmed. |
| SUP-PACK-003 | 嘉澳 | disposable-food-packaging | | factory | yes | yes | yes | Damon-confirmed | Damon-provided: mainly MFPP food containers. MFPP exact English/material/process definition remains unconfirmed and must not be expanded or guessed. |
| SUP-PACK-004 | 泰合 | disposable-food-packaging | | factory | yes | yes | yes | Damon-confirmed | Damon-provided: mainly injection-molded food containers. |

## Field Notes / 字段说明

- `supplier_id` — 供应商唯一 ID
- `public_name` — 仅当 Damon 明确允许公开时填写
- `category` — 品类
- `district` — 未知时留空，**不猜**
- `type` — `showroom-integrator` / `factory-backed-showroom` / `factory`
- `factory` — yes / no
- `shootable` — yes / no
- `public_identity_allowed` — yes / no
- `verified` — 本轮统一为 `Damon-confirmed`
- `note` — 只记录安全、可公开、非敏感事实

禁止写入：联系方式、内部价格、客户信息、地址（除非后续明确需要并确认公开）。
