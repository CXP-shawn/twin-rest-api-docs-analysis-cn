# 撤销 API 密钥

- 原文链接：<https://docs.twin.so/rest-api#revoke-an-api-key>
- 所属分组：**API Keys**
- 序号：#7

## 这篇讲了什么

本文档介绍如何通过 DELETE 请求永久撤销一个 API 密钥。撤销后，使用该密钥的所有请求将立即失效。调用时需在路径中传入目标密钥的 ID，并在请求头中携带有效的 API 密钥进行鉴权。成功响应将返回 revoked: true 以确认操作完成。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `DELETE` | `/api/public/v1/access-api-keys/{key_id}` | 撤销 API 密钥 | 永久撤销指定的 API 密钥，撤销后该密钥立即失效，无法再用于身份验证。 | `key_id` |

## 原文关键片段

> Permanently revokes an API key. Requests using it stop working immediately.

> DELETE /api/public/v1/access-api-keys/{key_id}

> "revoked": true

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
