# 将 Agent 移动到指定工作区

- 原文链接：<https://docs.twin.so/rest-api#move-agent-to-workspace>
- 所属分组：**Workspaces**
- 序号：#40

## 这篇讲了什么

本文档介绍了如何通过 REST API 将一个 Agent 从当前工作区迁移到另一个目标工作区。该接口使用 POST 方法，需要在路径中提供 agent_id，并在请求体中指定目标 workspace_id。认证通过请求头中的 x-api-key 完成。操作成功后返回 {"success": true}。适用于需要对 Agent 进行跨工作区管理的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/move` | Move Agent to Workspace | 将指定 Agent 从当前工作区迁移至目标工作区，需提供 Agent ID 和目标工作区 ID。 | `agent_id`, `workspace_id` |

## 原文关键片段

> POST /v1/agents/{agent_id}/move

> Moves an agent from its current workspace to a different one.

> "workspace_id": "proj_002"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
