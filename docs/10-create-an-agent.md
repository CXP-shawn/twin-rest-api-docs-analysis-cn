# 创建 Agent 接口

- 原文链接：<https://docs.twin.so/rest-api#create-an-agent>
- 所属分组：**Agents**
- 序号：#10

## 这篇讲了什么

本节介绍如何通过 POST 请求创建一个新的 Agent。请求体支持指定工作区、所有者、是否为子 Agent 以及派生来源等可选参数。成功后返回 201 状态码及完整的 Agent 对象，包含 agent_id、部署状态等关键字段。该接口适用于需要以编程方式初始化 Agent 实例的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents` | 创建 Agent | 创建一个新的 Agent 实例并返回完整的 Agent 对象，支持指定工作区、所有者及派生来源等可选参数。 | `workspace_id`, `owner_user_id`, `is_subagent`, `derived_from_agent_id`, `agent_id` |

## 原文关键片段

> POST /v1/agents

> Creates a new agent and returns the full agent object.

> "deployment_state": "not_deployed"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
