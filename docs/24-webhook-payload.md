# Webhook 负载结构说明

- 原文链接：<https://docs.twin.so/rest-api#webhook-payload>
- 所属分组：**Webhooks**
- 序号：#24

## 这篇讲了什么

本章节描述了 Twin 在订阅事件触发时向用户指定 Webhook URL 发送的 HTTP POST 请求的 JSON 负载格式。负载包含事件类型、事件触发时间戳以及与该事件相关的运行（run）详细数据。核心字段包括 event、timestamp 以及 data 对象下的 run_id、agent_id、status、outcome 和 finished_at。适用于需要实时接收 Agent 运行状态变更通知并进行后续处理的场景。

## 它暴露了什么

### 其他能力 / 概念

- **[webhook] Webhook Payload 结构** — 描述 Twin 触发事件时向 Webhook 地址推送的 JSON 请求体结构，包含事件类型、时间戳及运行详情等字段。 _(参数: `event`, `timestamp`, `data.run_id`, `data.agent_id`, `data.status`, `data.outcome`, `data.finished_at`)_

## 原文关键片段

> "event": "run.completed"

> "data.status": Run status: `in_progress`, `completed`, `error`, `stopped`, or `paused`

> "data.outcome": Present on `run.completed`: `success`, `partial`, or `fail`

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
