# 获取所有调度计划列表

- 原文链接：<https://docs.twin.so/rest-api#list-all-schedules>
- 所属分组：**Schedules**
- 序号：#31

## 这篇讲了什么

本文档介绍如何通过 GET 请求获取当前认证用户在所有 Agent 下的全部调度计划。请求时需在请求头中携带 API Key 进行身份验证。响应结果为一个包含所有调度计划的数组，每条记录包含关联的 Agent ID、cron 表达式以及暂停状态。适用于需要批量查询或管理定时任务的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/schedules` | List all schedules | 获取当前认证用户在所有 Agent 下的全部调度计划列表，返回包含 agent_id、cron 表达式及暂停状态的数组。 | `x-api-key`, `agent_id`, `cron`, `paused` |

## 原文关键片段

> GET /v1/schedules

> Returns all schedules for the authenticated user across all agents.

> "cron": "0 0 9 * * * *"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
