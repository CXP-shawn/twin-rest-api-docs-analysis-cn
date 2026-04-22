# 列出 API 密钥

- 原文链接：<https://docs.twin.so/rest-api#list-api-keys>
- 所属分组：**API Keys**
- 序号：#5

## 这篇讲了什么

本文档介绍了如何通过 GET 请求列出当前已认证用户的所有 API 密钥。调用时需在请求头中携带 x-api-key 进行身份验证。返回结果为一个 keys 数组，每条记录包含密钥 ID、名称、显示前缀及创建和最后使用时间。适用于需要管理或审计 API 密钥的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/api/public/v1/access-api-keys` | List API Keys | 获取当前认证用户的所有 API 密钥列表，返回包含密钥元信息的数组。 | `key_id`, `name`, `display_prefix`, `created_at`, `last_used_at` |

## 原文关键片段

> GET /api/public/v1/access-api-keys

> Returns all API keys for the authenticated user.

> "display_prefix": "tw_live_abc..."

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
