# 获取 Agent 调度计划

- 原文链接：<https://docs.twin.so/rest-api#get-agent-schedule>
- 所属分组：**Schedules**
- 序号：#26

## 这篇讲了什么

本文档介绍如何通过 GET 请求获取指定 Agent 的当前调度计划。调用时需要提供 agent_id 路径参数和 API 密钥进行认证。响应中包含 cron 表达式和暂停状态字段。如果该 Agent 尚未设置调度计划，则返回 schedule 为 null 的响应体。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/schedule` | Get Agent Schedule | 获取指定 Agent 的当前调度计划，返回 cron 表达式及其暂停状态，若无调度计划则返回 null。 | `agent_id` |

## 原文关键片段

> Returns the current schedule for an agent, if one exists.

> Returns `{"schedule": null}` if no schedule is set.

> "cron": "0 0 9 * * * *"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
