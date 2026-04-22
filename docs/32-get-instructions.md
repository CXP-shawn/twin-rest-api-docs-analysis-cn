# 获取 Agent 指令

- 原文链接：<https://docs.twin.so/rest-api#get-instructions>
- 所属分组：**Instructions**
- 序号：#32

## 这篇讲了什么

本章节介绍如何通过 REST API 获取指定 Agent 当前的指令内容。调用方需提供 agent_id 路径参数以及 API Key 进行鉴权。接口返回包含 instructions.content 字段的 JSON 对象，描述该 Agent 的行为规则。适用于需要查看或审计 Agent 当前配置指令的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/agents/{agent_id}/instructions` | Get instructions | 获取指定 Agent 当前绑定的指令内容，返回包含 content 字段的 instructions 对象。 | `agent_id`, `x-api-key` |

## 原文关键片段

> GET /v1/agents/{agent_id}/instructions

> Returns the current instructions for an agent.

> "content": "Check email every morning and summarize unread messages."

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
