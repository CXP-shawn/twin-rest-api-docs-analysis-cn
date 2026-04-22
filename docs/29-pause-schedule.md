# 暂停 Agent 调度计划

- 原文链接：<https://docs.twin.so/rest-api#pause-schedule>
- 所属分组：**Schedules**
- 序号：#29

## 这篇讲了什么

本文档介绍如何通过 POST 请求暂停指定 Agent 的调度计划。暂停后，调度配置会被保留，但不会触发新的运行，直到调度被恢复为止。适用于需要临时停止 Agent 自动执行任务的场景。请求需要携带 API Key 进行身份验证，响应返回操作是否成功的状态。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/schedule/pause` | 暂停 Agent 调度计划 | 暂停指定 Agent 的调度计划，调度配置保留但停止触发运行，直到恢复为止。 | `agent_id` |

## 原文关键片段

> Pauses the agent's schedule. The schedule is retained but will not trigger runs until resumed.

> curl -X POST https://build.twin.so/v1/agents/agent_abc123/schedule/pause

> "success": true

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
