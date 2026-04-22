# 更新 Webhook

- 原文链接：<https://docs.twin.so/rest-api#update-a-webhook>
- 所属分组：**Webhooks**
- 序号：#22

## 这篇讲了什么

本文档介绍如何通过 PATCH 请求更新指定 Agent 下的 Webhook 配置。支持更新的字段包括目标 URL、订阅的事件类型以及 Webhook 的启用状态。所有请求体字段均为可选，仅提供的字段会被修改。适用于需要动态调整 Webhook 订阅内容或临时禁用 Webhook 的场景。响应会返回完整的 Webhook 对象，包含更新后的状态和时间戳。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `PATCH` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | 更新 Webhook | 更新指定 Agent 下某个 Webhook 的 URL、事件订阅或启用状态，所有字段均为可选，仅传入字段生效。 | `agent_id`, `webhook_id`, `url`, `events`, `status` |

## 原文关键片段

> PATCH /v1/agents/{agent_id}/webhooks/{webhook_id}

> Updates a webhook's URL, subscribed events, or status. All fields are optional — only provided fields are changed.

> "status": "active" or "disabled"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
