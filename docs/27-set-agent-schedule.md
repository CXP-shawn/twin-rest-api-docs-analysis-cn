# 设置 Agent 定时调度

- 原文链接：<https://docs.twin.so/rest-api#set-agent-schedule>
- 所属分组：**Schedules**
- 序号：#27

## 这篇讲了什么

本文档介绍如何通过 PUT 请求为指定 Agent 创建或替换 Cron 定时调度。适用于需要定期自动执行 Agent 任务的场景。调用前提是 Agent 必须已处于已部署（deployed）状态。Twin 使用 7 字段格式的 Cron 表达式，字段依次为秒、分、时、日、月、周、年。请求成功后返回 {"success": true}。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `PUT` | `/v1/agents/{agent_id}/schedule` | Set Agent Schedule | 为指定 Agent 创建或替换 Cron 定时调度，需要提供 7 字段格式的 Cron 表达式，Agent 必须已部署。 | `agent_id`, `cron` |

## 原文关键片段

> Twin uses 7-field cron expressions: `sec min hour day month day-of-week year`

> cron expression (7-field format)

> The agent must be deployed.

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
