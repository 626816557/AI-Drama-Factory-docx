

> Version：V1.0
>
> Status：Draft
>
> Last Update：2026-07-01
>
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？

本文档回答：

> **AI Drama Factory 应如何统一接入 GPT 系列模型，并将 GPT 能力纳入 Factory AI Capability Layer？**

GPT Adapter（GPT 适配器）。

负责统一管理：

OpenAI GPT 系列能力。

包括：

- Chat Completion
- Structured Output
- Reasoning
- Vision（未来）
- Image Generation（GPT Image）
- Function Calling（未来）

GPT。

只是 Factory 的一个 AI Provider。

而不是 Factory 的核心。

---

# 二、GPT Adapter 定位（Position）

GPT Adapter。

不是：

OpenAI SDK。

也不是：

HTTP API 封装。

GPT Adapter。

是整个 Factory 的 GPT Capability Adapter。

负责：

统一接入。

统一管理。

统一调用。

全部 GPT 能力。

---

# 三、设计目标（Purpose）

GPT Adapter 的目标不是：

完成一次 API 调用。

而是：

建立统一。

稳定。

可维护。

可扩展。

的 GPT Integration Layer。

确保 Factory。

能够长期使用 GPT。

同时保持与业务解耦。

---

# 四、输入（Input）

GPT Adapter 输入：

- Capability Request
- Prompt
- Context
- System Prompt
- Parameters
- Output Schema（可选）

统一称为：

GPT Request。

---

# 五、输出（Output）

GPT Adapter 输出：

GPT Response。

包括：

- Result
- Usage
- Cost
- Latency
- Finish Reason
- Metadata
- Status

所有结果。

统一转换为：

Factory Standard Response。

---

# 六、核心职责（Responsibilities）

GPT Adapter 负责：

## Request Translation

将 Factory Request。

转换为 GPT Request。

---

## GPT Invocation

统一调用：

GPT Provider。

---

## Response Normalization

统一返回：

Factory Response。

避免上层依赖 GPT 格式。

---

## Error Handling

统一处理：

- Timeout
- Rate Limit
- Authentication
- Invalid Request
- Service Unavailable

统一错误格式。

统一重试策略。

---

## Usage Collection

统一统计：

- Token Usage
- Cost
- Latency
- Success Rate

供：

Analytics。

Monitoring。

Billing。

统一使用。

---

# 七、标准流程（Workflow）

Factory 推荐统一流程：

Receive GPT Request

↓

Validate Request

↓

Invoke GPT

↓

Receive Response

↓

Normalize Response

↓

Return Factory Response

---

# 八、设计原则（Design Principles）

Factory 坚持：

## Provider Independent

GPT。

只是 Provider。

---

## Capability First

Factory 关注：

Language Capability。

而不是：

GPT 本身。

---

## Unified Interface

统一接口。

---

## Standard Response

统一响应结构。

---

## Replaceable

任何时候。

GPT。

都可以被其它 Provider 替换。

---

# 九、Non-Goals（非目标）

本章不负责：

- Prompt Design
- Business Logic
- Workflow Scheduling
- Workshop Logic

这些能力。

将在其它章节定义。

---

# 十、Dependencies（依赖关系）

Depends On：

- 800 Model Adapter
- 809 LLM Router

Affects：

- Market Workshop
- Story Workshop
- Validation Workshop
- Director Workshop
- Learning Workshop

GPT Adapter。

负责 Factory 的 GPT 能力接入。

---

# 十一、本章总结

GPT Adapter。

不是：

OpenAI SDK。

也不是：

API Wrapper。

它负责：

统一管理 GPT 能力。

统一提供标准接口。

统一返回 Factory Response。

确保 GPT。

能够作为 Factory AI Capability Layer 的一个可替换 Provider。

---

**End**