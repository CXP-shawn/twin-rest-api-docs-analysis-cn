# 身份认证

- 原文链接：<https://docs.twin.so/rest-api#authentication>
- 所属分组：**Authentication**
- 序号：#3

## 这篇讲了什么

本节介绍 Twin REST API 的身份认证方式。每个请求都需要在 HTTP 请求头中携带 x-api-key 字段，值为用户的 API 密钥。API 密钥可以通过 Twin 控制台（builder.twin.so）生成，也可以通过 API 接口本身生成。适用于所有需要调用 Twin REST API 的场景。

## 它暴露了什么

### 其他能力 / 概念

- **[auth] API Key 认证** — 在每个请求的 HTTP 请求头中传入 x-api-key 字段以完成身份验证。 _(参数: `x-api-key`)_

## 原文关键片段

> x-api-key: YOUR_API_KEY

> Generate an API key from your Twin account or via the API itself

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
