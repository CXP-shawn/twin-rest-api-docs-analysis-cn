# 更新智能体指令

- 原文链接：<https://docs.twin.so/rest-api#update-instructions>
- 所属分组：**Instructions**
- 序号：#33

## 这篇讲了什么

本文档介绍了如何通过 PUT 请求更新指定智能体的指令内容。每次更新都会在历史记录中创建一个新版本，支持版本追踪。请求需要提供新的指令文本，并可选填写更新来源类型和来源标识符。该接口适用于需要动态调整智能体行为逻辑的场景，例如通过 API 或构建器修改任务描述。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `PUT` | `/v1/agents/{agent_id}/instructions` | Update instructions（更新指令） | 替换指定智能体的指令内容，每次调用均会生成新的历史版本记录，成功后返回 {"success": true}。 | `agent_id`, `content`, `source_type`, `source_id` |

## 原文关键片段

> Replaces the agent's instructions. Each update creates a new version in the history.

> curl -X PUT https://build.twin.so/v1/agents/agent_abc123/instructions

> "content": "Check email and Slack every morning."

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
