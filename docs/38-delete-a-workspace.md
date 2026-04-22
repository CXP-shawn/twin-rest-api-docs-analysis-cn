# 删除工作区

- 原文链接：<https://docs.twin.so/rest-api#delete-a-workspace>
- 所属分组：**Workspaces**
- 序号：#38

## 这篇讲了什么

本文档介绍如何通过 DELETE 请求永久删除一个指定的工作区及其内部所有 Agent。调用时需在路径中传入目标工作区的 ID，并在请求头中携带 API Key 进行鉴权。操作成功后接口返回 deleted: true 表示删除已完成。该操作不可逆，适用于需要清理整个工作区及其所有关联资源的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/v1/workspaces/{workspace_id}` | 删除工作区 | 永久删除指定工作区及其内部所有 Agent，操作不可逆，成功返回 deleted: true。 | `workspace_id`, `x-api-key` |

## 原文关键片段

> DELETE /v1/workspaces/{workspace_id}

> This permanently deletes the workspace and all agents within it.

> "deleted": true

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
