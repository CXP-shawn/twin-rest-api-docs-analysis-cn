# 重新排序工作区

- 原文链接：<https://docs.twin.so/rest-api#reorder-workspaces>
- 所属分组：**Workspaces**
- 序号：#39

## 这篇讲了什么

本文档介绍如何通过 API 对工作区进行重新排序。调用该接口可以设置工作区在界面中的显示顺序。请求体中需要传入按期望顺序排列的工作区 ID 数组。接口成功执行后返回 success: true。适用于需要自定义工作区展示顺序的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/workspaces/reorder` | 重新排序工作区 Reorder Workspaces | 通过传入有序的工作区 ID 数组，设置工作区的显示顺序，成功后返回 {"success": true}。 | `workspace_ids` |

## 原文关键片段

> Sets the display order of workspaces.

> workspace_ids: Workspace IDs in the desired order

> {"success": true}

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
