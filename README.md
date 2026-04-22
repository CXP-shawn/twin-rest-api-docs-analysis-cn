# Twin REST API 中文结构化分析

> 数据来源：<https://docs.twin.so/rest-api>
> 分析时间戳：2026-04-22 UTC
> 覆盖文档章节数：43
> 提取到的端点总数：39

## 项目说明

本仓库是对 Twin 官方 REST API 文档的**逐章节中文结构化分析**。源文档是一个带有深度锚点目录的单页文档（Mintlify 风格），我们按照一级锚点（H2 大分组）与二级锚点（H3 端点/子主题）将其切分为 43 个分析单元，分别使用大模型提取「这篇讲了什么」与「暴露了什么能力」，并保留了关键英文原文片段。

每份 `docs/*.md` 都是一个可独立阅读的中文解读文档，标题、摘要与说明全部使用中文，API 路径、参数名、代码片段与 notable_quotes 保留英文原文以便对照官方规范。

## 目录

### Base URL

- [基础 URL](docs/01-base-url.md)

### OpenAPI Specification

- [OpenAPI 规范说明](docs/02-openapi-specification.md)

### Authentication

- [身份认证](docs/03-authentication.md)

### Error Handling

- [错误处理规范](docs/04-error-handling.md)

### API Keys

- [列出 API 密钥](docs/05-list-api-keys.md)
- [创建 API 密钥](docs/06-create-an-api-key.md)
- [撤销 API 密钥](docs/07-revoke-an-api-key.md)

### Identity

- [获取当前用户信息](docs/08-get-current-user.md)

### Agents

- [列出 Agent 列表](docs/09-list-agents.md)
- [创建 Agent 接口](docs/10-create-an-agent.md)
- [获取单个 Agent 详情](docs/11-get-an-agent.md)
- [删除 Agent](docs/12-delete-an-agent.md)

### Runs

- [列出运行记录](docs/13-list-runs.md)
- [启动一个 Run](docs/14-start-a-run.md)
- [删除指定运行记录](docs/15-delete-a-run.md)
- [取消运行中的 Run](docs/16-cancel-a-run.md)

### Events

- [列出运行事件](docs/17-list-run-events.md)

### Webhooks

- [Webhook 事件类型](docs/18-event-types.md)
- [创建 Webhook](docs/19-create-a-webhook.md)
- [列出 Webhook 列表](docs/20-list-webhooks.md)
- [获取指定 Webhook 详情](docs/21-get-a-webhook.md)
- [更新 Webhook](docs/22-update-a-webhook.md)
- [删除 Webhook](docs/23-delete-a-webhook.md)
- [Webhook 负载结构说明](docs/24-webhook-payload.md)
- [Webhook 签名验证](docs/25-verifying-webhook-signatures.md)

### Schedules

- [获取 Agent 调度计划](docs/26-get-agent-schedule.md)
- [设置 Agent 定时调度](docs/27-set-agent-schedule.md)
- [删除Agent调度计划](docs/28-delete-agent-schedule.md)
- [暂停 Agent 调度计划](docs/29-pause-schedule.md)
- [恢复计划调度](docs/30-resume-schedule.md)
- [获取所有调度计划列表](docs/31-list-all-schedules.md)

### Instructions

- [获取 Agent 指令](docs/32-get-instructions.md)
- [更新智能体指令](docs/33-update-instructions.md)
- [获取指令历史版本](docs/34-get-instructions-history.md)

### Workspaces

- [列出工作区](docs/35-list-workspaces.md)
- [创建工作区](docs/36-create-a-workspace.md)
- [更新工作区](docs/37-update-a-workspace.md)
- [删除工作区](docs/38-delete-a-workspace.md)
- [重新排序工作区](docs/39-reorder-workspaces.md)
- [将 Agent 移动到指定工作区](docs/40-move-agent-to-workspace.md)

### Quick Reference

- [Twin REST API 快速参考](docs/41-quick-reference.md)

### Need Help? 💬

- [需要帮助？联系支持团队](docs/42-null.md)

### We'd Love Your Feedback! 🙏

- [用户反馈入口](docs/43-null.md)


## 全站端点速查表

下表聚合了所有被提取到的 HTTP 端点（方法 + 路径），来源文档链接指向本仓库对应的中文分析文件：

| 方法 | 路径 | 名称 | 来源文档 |
| --- | --- | --- | --- |
| `GET` | `/api/public/v1/access-api-keys` | List API Keys | [列出 API 密钥](docs/05-list-api-keys.md) |
| `POST` | `/api/public/v1/access-api-keys` | 创建 API 密钥 | [创建 API 密钥](docs/06-create-an-api-key.md) |
| `DELETE` | `/api/public/v1/access-api-keys/{key_id}` | 撤销 API 密钥 | [撤销 API 密钥](docs/07-revoke-an-api-key.md) |
| `GET` | `/v1/me` | Get Current User | [获取当前用户信息](docs/08-get-current-user.md) |
| `GET` | `/v1/agents` | List Agents | [列出 Agent 列表](docs/09-list-agents.md) |
| `POST` | `/v1/agents` | 创建 Agent | [创建 Agent 接口](docs/10-create-an-agent.md) |
| `GET` | `/v1/agents/{agent_id}` | 获取指定 Agent 详情 | [获取单个 Agent 详情](docs/11-get-an-agent.md) |
| `DELETE` | `/v1/agents/{agent_id}` | 删除 Agent | [删除 Agent](docs/12-delete-an-agent.md) |
| `GET` | `/v1/agents/{agent_id}/runs` | List runs（列出运行记录） | [列出运行记录](docs/13-list-runs.md) |
| `POST` | `/v1/agents/{agent_id}/runs` | Start a Run | [启动一个 Run](docs/14-start-a-run.md) |
| `DELETE` | `/v1/agents/{agent_id}/runs/{run_id}` | Delete a Run | [删除指定运行记录](docs/15-delete-a-run.md) |
| `POST` | `/v1/agents/{agent_id}/runs/{run_id}/cancel` | 取消 Run | [取消运行中的 Run](docs/16-cancel-a-run.md) |
| `GET` | `/v1/agents/{agent_id}/runs/{run_id}/events` | 列出运行事件（List Run Events） | [列出运行事件](docs/17-list-run-events.md) |
| `POST` | `/v1/agents/{agent_id}/webhooks` | 创建 Webhook | [创建 Webhook](docs/19-create-a-webhook.md) |
| `GET` | `/v1/agents/{agent_id}/webhooks` | 列出 Webhooks | [列出 Webhook 列表](docs/20-list-webhooks.md) |
| `GET` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | Get a Webhook | [获取指定 Webhook 详情](docs/21-get-a-webhook.md) |
| `PATCH` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | 更新 Webhook | [更新 Webhook](docs/22-update-a-webhook.md) |
| `DELETE` | `/v1/agents/{agent_id}/webhooks/{webhook_id}` | 删除 Webhook | [删除 Webhook](docs/23-delete-a-webhook.md) |
| `GET` | `/v1/agents/{agent_id}/schedule` | Get Agent Schedule | [获取 Agent 调度计划](docs/26-get-agent-schedule.md) |
| `PUT` | `/v1/agents/{agent_id}/schedule` | Set Agent Schedule | [设置 Agent 定时调度](docs/27-set-agent-schedule.md) |
| `DELETE` | `/v1/agents/{agent_id}/schedule` | Delete Agent Schedule | [删除Agent调度计划](docs/28-delete-agent-schedule.md) |
| `POST` | `/v1/agents/{agent_id}/schedule/pause` | 暂停 Agent 调度计划 | [暂停 Agent 调度计划](docs/29-pause-schedule.md) |
| `POST` | `/v1/agents/{agent_id}/schedule/resume` | Resume Schedule（恢复调度） | [恢复计划调度](docs/30-resume-schedule.md) |
| `GET` | `/v1/schedules` | List all schedules | [获取所有调度计划列表](docs/31-list-all-schedules.md) |
| `GET` | `/v1/agents/{agent_id}/instructions` | Get instructions | [获取 Agent 指令](docs/32-get-instructions.md) |
| `PUT` | `/v1/agents/{agent_id}/instructions` | Update instructions（更新指令） | [更新智能体指令](docs/33-update-instructions.md) |
| `GET` | `/v1/agents/{agent_id}/instructions/history` | Get instructions history | [获取指令历史版本](docs/34-get-instructions-history.md) |
| `GET` | `/v1/workspaces` | List Workspaces | [列出工作区](docs/35-list-workspaces.md) |
| `POST` | `/v1/workspaces` | Create a Workspace | [创建工作区](docs/36-create-a-workspace.md) |
| `PUT` | `/v1/workspaces/{workspace_id}` | Update a Workspace | [更新工作区](docs/37-update-a-workspace.md) |
| `DELETE` | `/v1/workspaces/{workspace_id}` | 删除工作区 | [删除工作区](docs/38-delete-a-workspace.md) |
| `POST` | `/v1/workspaces/reorder` | 重新排序工作区 Reorder Workspaces | [重新排序工作区](docs/39-reorder-workspaces.md) |
| `POST` | `/v1/agents/{agent_id}/move` | Move Agent to Workspace | [将 Agent 移动到指定工作区](docs/40-move-agent-to-workspace.md) |
| `GET` | `/v1/me` | 获取当前用户 | [Twin REST API 快速参考](docs/41-quick-reference.md) |
| `GET` | `/v1/agents` | Agent 管理 | [Twin REST API 快速参考](docs/41-quick-reference.md) |
| `POST` | `/v1/agents/{agent_id}/runs` | Run（运行任务）管理 | [Twin REST API 快速参考](docs/41-quick-reference.md) |
| `PUT` | `/v1/agents/{agent_id}/schedule` | 定时任务（Schedule）管理 | [Twin REST API 快速参考](docs/41-quick-reference.md) |
| `GET` | `/v1/agents/{agent_id}/instructions` | Agent 指令管理 | [Twin REST API 快速参考](docs/41-quick-reference.md) |
| `GET` | `/v1/workspaces` | 工作区（Workspace）管理 | [Twin REST API 快速参考](docs/41-quick-reference.md) |


共计 **39** 个端点。

## 整体架构小结

Twin REST API 以 https://build.twin.so 为根域，采用 /v1 版本前缀与标准 RESTful URL 风格，并提供符合 OpenAPI 3.1 标准的机器可读规范文件，方便自动生成客户端或导入调试工具。鉴权统一通过请求头 x-api-key 传递，密钥可由控制台或 API 自身创建、列举及撤销，生命周期管理完整。核心资源围绕 Workspace → Agent → Run → Event 形成清晰的层级关系：Workspace 用于组织隔离，Agent 代表可部署的智能体实例，Run 记录每次执行过程，Event 提供运行内部的细粒度追踪；Webhook 订阅 Run 的生命周期事件以支持异步通知，Schedule 通过七字段 Cron 表达式驱动 Agent 定时执行，Instructions 则支持版本化的指令内容管理。亮点方面，错误处理遵循 RFC 9457 Problem Details 规范，Webhook 推送采用 HMAC-SHA256 签名验证以防伪造，指令历史版本机制便于审计回溯，整体设计较为规范且可扩展。需要注意的是，部分资源（如 API Keys 路径为 /api/public/v1/，与其余资源的 /v1/ 前缀不一致）存在路径风格不统一的问题，可能增加客户端集成的维护成本；此外，Webhook 签名头使用了非标准前缀 X-Cobb-，暗示存在内部命名与对外品牌不一致的历史遗留痕迹，文档也提示开发者注意旧版错误格式的迁移，说明 API 仍处于持续演进阶段。

## 文件结构

```
.
├── README.md                       # 本文件：项目说明 + 目录 + 端点速查表 + 架构小结
└── docs/
    ├── 01-base-url.md              # 逐章节中文分析，序号与原文顺序保持一致
    ├── 02-openapi-specification.md
    ├── ...
    └── 43-xxx.md
```

### 每份 `docs/*.md` 的内容约定

1. `# 中文标题` — 由大模型翻译/润色的中文标题
2. 原文链接（回到 Twin 官方文档对应锚点）、所属分组、序号
3. `## 这篇讲了什么` — 3-6 句中文摘要
4. `## 它暴露了什么` — 先列 endpoint 表格（方法 / 路径 / 名称 / 说明 / 关键参数），再列其他能力/概念（auth、concept、webhook、error_code 等）
5. `## 原文关键片段` — 英文原文引用（最多 3 条）

## 许可与声明

- 本仓库内容为对公开文档的**结构化再加工**，不包含任何 Twin 内部实现代码。
- 所有英文片段版权归 Twin 所有；中文摘要与分析文本由 AI 自动生成，可能存在个别误读，以官方文档为准。
- 如发现错误，欢迎提 Issue。
