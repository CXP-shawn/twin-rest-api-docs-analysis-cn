# 错误处理规范

- 原文链接：<https://docs.twin.so/rest-api#error-handling>
- 所属分组：**Error Handling**
- 序号：#4

## 这篇讲了什么

本节描述 Twin REST API 的错误响应格式，遵循 RFC 9457 Problem Details 标准，响应 Content-Type 为 application/problem+json。错误响应体包含 type、status、title、detail 四个字段，分别表示问题类型 URI、HTTP 状态码、标准原因短语和可读错误信息。当 type 为 about:blank 时，表示错误语义与 HTTP 状态码本身一致，无额外扩展含义。文档还提示从旧版 error.code/error.message 格式迁移的开发者需要更新错误解析逻辑。

## 它暴露了什么

### 其他能力 / 概念

- **[error_code] RFC 9457 Problem Details 错误响应格式** — Twin API 使用符合 RFC 9457 的 Problem Details 格式返回错误，包含 type、status、title、detail 字段，替代旧版 error.code/error.message 结构。 _(参数: `type`, `status`, `title`, `detail`)_

## 原文关键片段

> Error responses follow RFC 9457 Problem Details and return `Content-Type: application/problem+json`

> type` is a URI identifying the problem type (`about:blank` means no extra semantics beyond the HTTP status)

> If you are migrating from the previous `error.code` / `error.message` format, update your error parsing logic.

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
