# Twin REST API 快速参考

- 原文链接：<https://docs.twin.so/rest-api#quick-reference>
- 所属分组：**Quick Reference**
- 序号：#41

## 这篇讲了什么

本章节提供 Twin REST API 的完整端点速查表，涵盖 API 密钥管理、Agent 管理、运行任务、Webhook、定时任务、指令及工作区等所有主要资源。所有 Agent、Run 和 Event 相关接口均已版本化，位于 /v1 路径下并遵循标准 HTTP 方法规范。适用于需要快速查阅接口路径与方法的开发者。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/me` | 获取当前用户 | 获取当前认证用户信息。 | — |
| `GET` | `/v1/agents` | Agent 管理 | 对 Agent 进行增删查操作，支持列表、创建、获取和删除。 | `agent_id` |
| `POST` | `/v1/agents/{agent_id}/runs` | Run（运行任务）管理 | 在指定 Agent 下启动、取消、删除运行任务及查看运行事件。 | `agent_id`, `run_id` |
| `PUT` | `/v1/agents/{agent_id}/schedule` | 定时任务（Schedule）管理 | 为 Agent 设置、获取、删除、暂停和恢复定时任务，也可列出所有定时任务。 | `agent_id` |
| `GET` | `/v1/agents/{agent_id}/instructions` | Agent 指令管理 | 获取、更新和查看 Agent 指令历史记录。 | `agent_id` |
| `GET` | `/v1/workspaces` | 工作区（Workspace）管理 | 对工作区进行增删改、重新排序以及在工作区间移动 Agent。 | `workspace_id`, `agent_id` |

### 其他能力 / 概念

- **[auth] API 密钥管理** — 列出、创建和撤销 API 密钥，用于访问控制。 _(参数: `key_id`)_ `/api/public/v1/access-api-keys`
- **[webhook] Webhook 管理** — 为 Agent 创建、查询、更新和删除 Webhook 订阅。 _(参数: `agent_id`, `webhook_id`)_ `/v1/agents/{agent_id}/webhooks`

## 原文关键片段

> Agent, run, and event APIs are now versioned REST endpoints under `/v1` with standard HTTP methods.

> Get your API key — Sign in to Twin to generate your API key and start building.

> | List API keys | `GET` | `/api/public/v1/access-api-keys` |

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
