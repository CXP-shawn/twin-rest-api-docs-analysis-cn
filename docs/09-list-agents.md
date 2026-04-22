# 列出 Agent 列表

- 原文链接：<https://docs.twin.so/rest-api#list-agents>
- 所属分组：**Agents**
- 序号：#9

## 这篇讲了什么

本文档介绍了如何通过 GET 请求获取当前已认证用户的 Agent 列表。支持按工作区过滤，并提供游标分页功能以控制返回数量。响应结果包含每个 Agent 的基本状态信息，如最近运行 ID、是否已完成以及部署状态。适用于需要批量查询和管理已有 Agent 的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents` | List Agents | 获取当前认证用户下的所有 Agent 列表，支持工作区筛选和分页控制，返回每个 Agent 的状态摘要信息。 | `workspace_id`, `cursor`, `limit` |

## 原文关键片段

> Returns agents for the authenticated user, with optional pagination and workspace filtering.

> curl "https://build.twin.so/v1/agents?limit=20" -H "x-api-key: YOUR_API_KEY"

> "deployment_state": "deployed"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
