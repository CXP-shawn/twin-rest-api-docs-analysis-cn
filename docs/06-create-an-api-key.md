# 创建 API 密钥

- 原文链接：<https://docs.twin.so/rest-api#create-an-api-key>
- 所属分组：**API Keys**
- 序号：#6

## 这篇讲了什么

本文档介绍如何通过 POST 请求创建一个新的 Twin API 密钥。创建成功后，完整的密钥字符串仅在响应中返回一次，需立即妥善保存。请求体只需提供密钥名称（name），响应中包含密钥 ID、名称、完整密钥、显示前缀及创建时间戳。适用于需要为集成或自动化场景生成新访问凭证的场景。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `POST` | `/api/public/v1/access-api-keys` | 创建 API 密钥 | 创建一个新的 API 访问密钥，完整密钥仅在创建时返回一次，需立即安全存储。 | `name`, `key_id`, `api_key`, `display_prefix`, `created_at` |

## 原文关键片段

> The full key is only returned once, so store it securely.

> The `api_key` field is only returned at creation time. Store it immediately.

> curl -X POST https://build.twin.so/api/public/v1/access-api-keys

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
