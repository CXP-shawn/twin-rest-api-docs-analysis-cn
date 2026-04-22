# 获取当前用户信息

- 原文链接：<https://docs.twin.so/rest-api#get-current-user>
- 所属分组：**Identity**
- 序号：#8

## 这篇讲了什么

本节介绍如何通过 Twin REST API 获取当前已认证用户的基本信息。适用于需要验证 API Key 归属或获取用户标识的场景。请求需在请求头中携带 API Key，接口返回对应的用户 ID。属于身份认证类基础接口。

## 它暴露了什么

### 端点

| 方法 | 路径 | 名称 | 说明 | 关键参数 |
| --- | --- | --- | --- | --- |
| `GET` | `/v1/me` | Get Current User | 返回当前 API Key 对应的已认证用户 ID，适用于身份验证和用户归属确认。 | `x-api-key`, `user_id` |

## 原文关键片段

> GET /v1/me

> Returns the authenticated user ID.

> curl https://build.twin.so/v1/me \
>   -H "x-api-key: YOUR_API_KEY"

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
