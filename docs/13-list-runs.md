# 列出运行记录

- 原文链接：<https://docs.twin.so/rest-api#list-runs>
- 所属分组：**Runs**
- 序号：#13

## 这篇讲了什么

本章节介绍如何通过 GET 请求获取某个智能体（agent）的历史运行记录。支持分页查询，并提供多种过滤参数，包括按运行状态、运行 ID、启动时间范围、策略类型和策略分组进行筛选。响应结果包含运行列表及总记录数等分页信息，适用于监控和审计 agent 的运行历史。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/runs` | List runs（列出运行记录） | 获取指定 agent 的历史运行记录，支持分页与多条件过滤，返回运行列表及分页信息。 | `agent_id`, `page`, `page_size`, `filter_status`, `filter_run_id`, `filter_started_after`, `filter_started_before`, `filter_policy_type`, `filter_policy_group` |

## 原文关键片段

> Returns run history for an agent.

> filter_policy_group filter (builder/runner)

> ISO-8601 lower bound / upper bound

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
