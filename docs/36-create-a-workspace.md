# 创建工作区

- 原文链接：<https://docs.twin.so/rest-api#create-a-workspace>
- 所属分组：**Workspaces**
- 序号：#36

## 这篇讲了什么

本节文档介绍如何通过 REST API 创建一个新的工作区（Workspace）。调用方需提供工作区名称，并在请求头中携带 API Key 进行鉴权。请求成功后返回 201 状态码及新建工作区的 ID 和名称信息。适用于需要以编程方式批量或自动化创建工作区的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/workspaces` | Create a Workspace | 创建一个新的工作区，需在请求体中提供工作区名称，成功后返回工作区 ID 和名称。 | `name` |

## 原文关键片段

> POST /v1/workspaces

> x-api-key: YOUR_API_KEY

> 201 Created

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
