# 获取指令历史版本

- 原文链接：<https://docs.twin.so/rest-api#get-instructions-history>
- 所属分组：**Instructions**
- 序号：#34

## 这篇讲了什么

该文档描述了如何通过 GET 请求获取某个 Agent 的历史指令版本列表。适用于需要审计或回溯 Agent 指令变更记录的场景。请求支持通过 limit 参数限制返回的版本数量，默认返回全部历史版本。响应结果以数组形式返回每个历史版本的内容及创建时间。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/instructions/history` | Get instructions history | 获取指定 Agent 的历史指令版本列表，返回每个版本的内容及创建时间。 | `agent_id`, `limit` |

## 原文关键片段

> Returns previous versions of the agent's instructions.

> GET /v1/agents/{agent_id}/instructions/history?limit=10

> "instruction_versions": [{"content": "...", "created_at": "..."}]

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
