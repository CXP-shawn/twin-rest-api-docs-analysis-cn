# 删除 Agent

- 原文链接：<https://docs.twin.so/rest-api#delete-an-agent>
- 所属分组：**Agents**
- 序号：#12

## 这篇讲了什么

本文档介绍如何通过 DELETE 请求永久删除指定的 Agent 及其所有运行数据。调用时需在路径中提供 agent_id，并通过请求头传入 API 密钥进行认证。操作成功后返回 204 No Content（无响应体），若 Agent 不存在则返回 404 错误。适用于需要清理不再使用的 Agent 资源的场景，该操作不可逆。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/v1/agents/{agent_id}` | 删除 Agent | 永久删除指定 Agent 及其所有运行数据，成功返回 204，未找到返回 404。 | `agent_id` |

### 其他能力 / 概念

- **[auth] API Key 认证** — 通过请求头 x-api-key 传入 API 密钥以完成身份认证。 _(参数: `x-api-key`)_

## 原文关键片段

> Permanently deletes an agent and its run data.

> 204 No Content — empty body on success. Returns `404` if the agent was not found.

> curl -X DELETE https://build.twin.so/v1/agents/agent_abc123 \
>   -H "x-api-key: YOUR_API_KEY"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
