# 创建 Webhook

- 原文链接：<https://docs.twin.so/rest-api#create-a-webhook>
- 所属分组：**Webhooks**
- 序号：#19

## 这篇讲了什么

本文档描述如何为指定 Agent 注册一个 Webhook URL。调用该接口后，系统将返回一个签名密钥（signing_secret），该密钥仅在创建时返回一次，需立即妥善保存。通过订阅不同的事件类型（如 run.completed、run.failed），开发者可以实时接收 Agent 运行状态的通知。适用于需要异步监听 Agent 任务执行结果的集成场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/webhooks` | 创建 Webhook | 为指定 Agent 注册一个 Webhook 接收端点，返回包含一次性签名密钥的 Webhook 配置信息，用于后续验证入站事件签名。 | `agent_id`, `url`, `events`, `signing_secret`, `webhook_id`, `status`, `created_at` |

### 其他能力 / 概念

- **[auth] Webhook 签名密钥（signing_secret）** — 创建 Webhook 时返回的签名密钥，仅在响应中出现一次，用于验证后续所有入站 Webhook 请求的合法性。 _(参数: `signing_secret`)_
- **[concept] Webhook 事件类型** — 支持订阅的事件类型，包括 run.completed 和 run.failed，至少需要订阅一个事件类型才能成功创建 Webhook。 _(参数: `events`, `run.completed`, `run.failed`)_

## 原文关键片段

> The signing secret is returned **only once** in the response — store it immediately.

> The `signing_secret` is only returned at creation time. Store it securely — you need it to verify incoming webhook signatures.

> "events": ["run.completed", "run.failed"]

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
