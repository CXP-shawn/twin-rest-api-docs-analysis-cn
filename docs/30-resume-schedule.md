# 恢复计划调度

- 原文链接：<https://docs.twin.so/rest-api#resume-schedule>
- 所属分组：**Schedules**
- 序号：#30

## 这篇讲了什么

本文档介绍如何通过 REST API 恢复一个已暂停的 Agent 调度计划。适用场景为：当某个 Agent 的定时调度被暂停后，需要重新启动其自动执行流程。请求仅需提供路径参数 agent_id，并在请求头中携带 API Key 进行鉴权。响应结果为简单的 success 布尔值，表示操作是否成功。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/schedule/resume` | Resume Schedule（恢复调度） | 恢复指定 Agent 已暂停的调度计划，成功后返回 {"success": true}。 | `agent_id` |

## 原文关键片段

> POST /v1/agents/{agent_id}/schedule/resume

> curl -X POST https://build.twin.so/v1/agents/agent_abc123/schedule/resume

> "success": true

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
