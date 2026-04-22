# Webhook 签名验证

- 原文链接：<https://docs.twin.so/rest-api#verifying-webhook-signatures>
- 所属分组：**Webhooks**
- 序号：#25

## 这篇讲了什么

本章节介绍如何验证 Twin Webhook 请求的真实性。每次 Webhook 推送都会附带两个自定义 HTTP 头：X-Cobb-Signature（包含 HMAC-SHA256 签名）和 X-Cobb-Event（事件类型）。开发者需使用预共享的 signing_secret 对原始请求体计算 HMAC-SHA256，并与 header 中的签名比对，以防止伪造请求。文档还提供了 Node.js 示例代码，演示如何使用时序安全比较函数完成验证。

## 它暴露了什么

### 其他能力 / 概念

- **[webhook] Webhook 签名头** — Webhook 推送时携带的签名头，用于验证请求来源的真实性，值格式为 sha256=<十六进制字符串>。 _(参数: `X-Cobb-Signature`, `X-Cobb-Event`)_
- **[concept] HMAC-SHA256 签名验证机制** — 使用 HMAC-SHA256 算法对 signing_secret 和原始请求体进行哈希计算，并通过时序安全比较验证签名的完整性。 _(参数: `signing_secret`, `raw_request_body`, `signatureHeader`)_

## 原文关键片段

> X-Cobb-Signature: sha256=<hex HMAC-SHA256>

> compute HMAC-SHA256(signing_secret, raw_request_body) and compare it to the signature in the header

> crypto.timingSafeEqual(Buffer.from(expected), Buffer.from(signatureHeader))

---

_自动生成于 2026-04-22，来自 https://docs.twin.so/rest-api_
