# 删除 Webhook

- 原文链接：<https://docs.twin.so/rest-api#delete-a-webhook>
- 所属分组：**Webhooks**
- 序号：#23

## 这篇讲了什么

本文档介绍如何通过 DELETE 请求永久删除指定 Agent 下的某个 Webhook。删除后，该 Webhook 将不再接收任何事件推送。请求需要提供 agent_id 和 webhook_id 两个路径参数，并通过 x-api-key 进行身份认证。成功删除后，API 返回 204 No Content 状态码，无响应体。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | 删除 Webhook | 永久删除指定 Agent 下的某个 Webhook，删除后不再推送任何事件，成功返回 204 No Content。 | `agent_id`, `webhook_id` |

## 原文关键片段

> DELETE /v1/agents/{agent_id}/webhooks/{webhook_id}

> Permanently deletes a webhook. No further events will be delivered.

> 204 No Content

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
