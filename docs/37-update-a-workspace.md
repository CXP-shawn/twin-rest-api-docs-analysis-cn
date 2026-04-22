# 更新工作区

- 原文链接：<https://docs.twin.so/rest-api#update-a-workspace>
- 所属分组：**Workspaces**
- 序号：#37

## 这篇讲了什么

本文档介绍如何通过 PUT 请求更新指定工作区的基本信息，包括名称和图标配置。调用时需在路径中提供工作区 ID，并在请求体中传入新名称（必填）及可选的图标配置字符串。认证方式为在请求头中携带 API Key。适用于需要重命名或更换工作区图标的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `PUT` | `/v1/workspaces/{workspace_id}` | Update a Workspace | 更新指定工作区的名称或图标配置，返回更新后的工作区信息。 | `workspace_id`, `name`, `icon_config` |

### 其他能力 / 概念

- **[auth] API Key 认证** — 通过请求头 x-api-key 传递 API Key 进行身份认证。 _(参数: `x-api-key`)_

## 原文关键片段

> PUT /v1/workspaces/{workspace_id}

> Updates a workspace's name or icon.

> "name": "Renamed Workspace"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
