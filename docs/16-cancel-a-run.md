# 取消运行中的 Run

- 原文链接：<https://docs.twin.so/rest-api#cancel-a-run>
- 所属分组：**Runs**
- 序号：#16

## 这篇讲了什么

本文档介绍如何通过 POST 请求取消一个正在运行的 Run。该接口具有幂等性，对已完成的 Run 执行取消操作同样返回成功。请求体为可选项，可附带人类可读的取消原因。响应体通过 error 字段是否为空来表示操作结果。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/runs/{run_id}/cancel` | 取消 Run | 取消指定 Agent 下正在运行的 Run，支持幂等调用，可选传入取消原因。 | `agent_id`, `run_id`, `reason` |

## 原文关键片段

> Cancels a running run. The request is idempotent — cancelling an already-finished run returns success.

> An empty `error` means success. A non-empty value is informational (e.g. the run was already stopped).

> The body is entirely optional — you may send an empty object `{}` or omit the body altogether.

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
