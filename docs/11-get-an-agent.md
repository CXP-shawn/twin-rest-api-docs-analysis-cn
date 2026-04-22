# 获取单个 Agent 详情

- 原文链接：<https://docs.twin.so/rest-api#get-an-agent>
- 所属分组：**Agents**
- 序号：#11

## 这篇讲了什么

本文档描述了通过 Agent ID 获取特定 Agent 完整详情的 REST API 接口。调用方需在请求头中携带 API Key 进行身份认证。接口返回 Agent 的基本信息，包括最新运行记录 ID、最后活跃时间、部署状态及部署时间等关键字段。适用于需要查询特定 Agent 当前状态和运行情况的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}` | 获取指定 Agent 详情 | 通过 agent_id 路径参数获取指定 Agent 的完整详情，包括运行状态、部署信息等。 | `agent_id`, `latest_run_id`, `last_activity_at`, `latest_run_is_finished`, `has_runs`, `workspace_id`, `deployment_state`, `deployed_at` |

### 其他能力 / 概念

- **[auth] API Key 认证** — 请求需在 HTTP Header 中通过 x-api-key 字段传入 API Key 进行身份验证。 _(参数: `x-api-key`)_

## 原文关键片段

> GET /v1/agents/{agent_id}

> Returns full details for a specific agent.

> "deployment_state": "deployed"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
