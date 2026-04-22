# 列出 Webhook 列表

- 原文链接：<https://docs.twin.so/rest-api#list-webhooks>
- 所属分组：**Webhooks**
- 序号：#20

## 这篇讲了什么

本节介绍如何通过 GET 请求获取指定 Agent 下所有已注册的 Webhook。调用时需在路径中提供 agent_id，并通过 x-api-key 进行身份验证。返回结果包含每个 Webhook 的基本信息，如 webhook_id、订阅的事件类型、状态及时间戳。适用于需要查看或审计某个 Agent 当前 Webhook 配置的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/webhooks` | 列出 Webhooks | 获取指定 Agent 下注册的所有 Webhook 列表，返回包含 webhook_id、事件类型、状态等字段的数组。 | `agent_id` |

## 原文关键片段

> GET /v1/agents/{agent_id}/webhooks

> Returns all webhooks registered for the given agent.

> "events": ["run.completed", "run.failed"]

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
