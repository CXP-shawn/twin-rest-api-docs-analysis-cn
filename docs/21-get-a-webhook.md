# 获取指定 Webhook 详情

- 原文链接：<https://docs.twin.so/rest-api#get-a-webhook>
- 所属分组：**Webhooks**
- 序号：#21

## 这篇讲了什么

本文档介绍如何通过 GET 请求获取某个 Agent 下特定 Webhook 的详细信息。需要提供 agent_id 和 webhook_id 两个路径参数，并在请求头中携带 API Key 进行鉴权。接口返回 Webhook 的基本属性，包括 URL、事件列表、状态及时间戳等字段。适用于需要查询已注册 Webhook 配置详情的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | Get a Webhook | 获取指定 Agent 下某个 Webhook 的详细配置信息，包括 URL、事件类型、状态及创建/更新时间。 | `agent_id`, `webhook_id` |

### 其他能力 / 概念

- **[auth] API Key 鉴权** — 请求需在 Header 中携带 x-api-key 进行 API 密钥鉴权。 _(参数: `x-api-key`)_

## 原文关键片段

> GET /v1/agents/{agent_id}/webhooks/{webhook_id}

> Returns details for a specific webhook.

> "events": ["run.completed", "run.failed"]

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
