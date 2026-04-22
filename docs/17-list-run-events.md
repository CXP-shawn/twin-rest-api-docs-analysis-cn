# 列出运行事件

- 原文链接：<https://docs.twin.so/rest-api#list-run-events>
- 所属分组：**Events**
- 序号：#17

## 这篇讲了什么

该文档介绍了如何通过 GET 请求获取某个 Agent 特定运行（Run）过程中产生的事件列表。适用于需要追踪、监控或回放 Agent 运行过程的场景。请求路径需提供 agent_id 和 run_id 两个路径参数，并支持通过 limit 和 after_index 进行分页查询。返回结果为带有事件索引的事件数组，每个事件包含具体的事件类型（如 started）。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/runs/{run_id}/events` | 列出运行事件（List Run Events） | 获取指定 Agent 的某次运行所产生的所有事件，支持分页，可用于监控运行过程或增量拉取事件。 | `agent_id`, `run_id`, `limit`, `after_index` |

## 原文关键片段

> GET /v1/agents/{agent_id}/runs/{run_id}/events

> "after_index": Return events after this event index

> curl "https://build.twin.so/v1/agents/agent_abc123/runs/run_xyz789/events?limit=50"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
