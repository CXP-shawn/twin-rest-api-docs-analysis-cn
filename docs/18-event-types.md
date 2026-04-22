# Webhook 事件类型

- 原文链接：<https://docs.twin.so/rest-api#event-types>
- 所属分组：**Webhooks**
- 序号：#18

## 这篇讲了什么

本文档列出了 Twin REST API 中 Webhook 支持的所有事件类型。每个事件对应一个 run（任务执行）的不同生命周期状态，包括开始、完成、失败、停止和暂停。适用于需要监听任务执行状态变化并做出响应的集成场景。开发者可根据这些事件类型订阅相应的 Webhook，以便在任务状态发生变化时接收通知。

## 它暴露了什么

### 其他能力 / 概念

- **[webhook] run.started** — 当一个 run 开始执行时触发的 Webhook 事件。 _(参数: `run.started`)_
- **[webhook] run.completed** — 当一个 run 执行结束（无论成功、部分完成或失败）时触发的 Webhook 事件。 _(参数: `run.completed`)_
- **[webhook] run.failed** — 当一个 run 遇到策略错误时触发的 Webhook 事件。 _(参数: `run.failed`)_
- **[webhook] run.stopped** — 当一个 run 被用户手动停止时触发的 Webhook 事件。 _(参数: `run.stopped`)_
- **[webhook] run.paused** — 当一个 run 被用户暂停或由 agent 自动暂停（超过 15 分钟）时触发的 Webhook 事件。 _(参数: `run.paused`)_

## 原文关键片段

> run.started

> run.completed

> run.failed, run.stopped, run.paused

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
