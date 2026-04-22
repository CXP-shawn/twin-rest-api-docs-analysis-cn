# 删除Agent调度计划

- 原文链接：<https://docs.twin.so/rest-api#delete-agent-schedule>
- 所属分组：**Schedules**
- 序号：#28

## 这篇讲了什么

本章节介绍如何通过DELETE请求移除指定Agent的调度计划。适用于需要取消Agent自动执行任务的场景。请求需要在路径中提供agent_id，并通过API Key进行身份验证。成功响应返回{"success":true}的JSON对象。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/v1/agents/{agent_id}/schedule` | Delete Agent Schedule | 移除指定Agent的调度计划，取消该Agent的自动执行任务安排。 | `agent_id` |

## 原文关键片段

> DELETE /v1/agents/{agent_id}/schedule

> Removes the schedule from an agent.

> "success": true

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
