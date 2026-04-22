# 启动一个 Run

- 原文链接：<https://docs.twin.so/rest-api#start-a-run>
- 所属分组：**Runs**
- 序号：#14

## 这篇讲了什么

本文档描述了如何通过 POST 请求为已存在的 Agent 启动一次运行（Run）。调用者需提供 agent_id 作为路径参数，并可选传入运行模式、用户消息和是否跳过部署检查等请求体参数。接口成功后返回 201 状态码及包含 run_id、status、started_at 等字段的 Run 对象。适用于需要触发 Agent 执行特定工作流的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/v1/agents/{agent_id}/runs` | Start a Run | 为指定 Agent 启动一次新的运行任务，返回包含运行状态和元数据的 Run 对象。 | `agent_id`, `run_mode`, `user_message`, `skip_deploy_check` |

## 原文关键片段

> POST /v1/agents/{agent_id}/runs

> "run_mode": "run", "user_message": "Please execute the latest workflow."

> 201 Created

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
