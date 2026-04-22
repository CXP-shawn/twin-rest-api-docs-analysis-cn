# 列出工作区

- 原文链接：<https://docs.twin.so/rest-api#list-workspaces>
- 所属分组：**Workspaces**
- 序号：#35

## 这篇讲了什么

本节介绍如何通过 GET 请求获取当前认证用户下的所有工作区列表。调用时需在请求头中携带 API 密钥进行身份验证。响应结果以数组形式返回每个工作区的 ID 和名称。适用于需要枚举用户所有工作区的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/workspaces` | List Workspaces | 获取当前认证用户所属的全部工作区列表，返回每个工作区的 ID 与名称。 | `workspace_id`, `name` |

## 原文关键片段

> GET /v1/workspaces

> Returns all workspaces for the authenticated user.

> curl https://build.twin.so/v1/workspaces -H "x-api-key: YOUR_API_KEY"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
