# 删除指定运行记录

- 原文链接：<https://docs.twin.so/rest-api#delete-a-run>
- 所属分组：**Runs**
- 序号：#15

## 这篇讲了什么

本文档介绍如何通过 DELETE 请求删除某个 Agent 下的指定运行（Run）记录。调用时需在路径中提供 agent_id 和 run_id 两个必填参数。请求需携带 API Key 进行身份验证。成功删除后返回 204 No Content，若运行记录不存在则返回 404 错误。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/v1/agents/{agent_id}/runs/{run_id}` | Delete a Run | 删除指定 Agent 下的某条运行记录，成功返回 204，未找到返回 404。 | `agent_id`, `run_id` |

## 原文关键片段

> DELETE /v1/agents/{agent_id}/runs/{run_id}

> 204 No Content — empty body on success. Returns 404 if the run was not found.

> curl -X DELETE https://build.twin.so/v1/agents/agent_abc123/runs/run_xyz789 -H "x-api-key: YOUR_API_KEY"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
