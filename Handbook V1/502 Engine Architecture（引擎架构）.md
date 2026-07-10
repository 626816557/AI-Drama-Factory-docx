

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

> **AI Drama Factory 中，真正执行生产任务的能力应如何组织？**

Engine（引擎）。

是 Factory 的能力执行单元（Execution Unit）。

Workshop 负责组织业务。

Engine 负责执行能力。

Factory 的所有生产能力。

最终都由不同 Engine 完成。

---

# 二、设计目标（Purpose）

Engine Architecture 的目标不是：

管理业务流程。

而是：

建立统一的能力执行层。

让所有 Workshop。

无需关心具体模型。

具体服务。

具体供应商。

即可完成生产任务。

Engine 是连接：

业务。

与。

AI 能力。

之间的重要桥梁。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Capability-Oriented（能力导向）

Engine。

围绕能力设计。

而不是围绕模型设计。

例如：

Text Generation。

Image Generation。

Video Generation。

Translation。

TTS。

ASR。

每一种能力。

对应一种 Engine。

---

## Decoupling（业务解耦）

Workshop。

不直接调用：

GPT。

Claude。

Flux。

Seedream。

ComfyUI。

Workshop。

只调用对应 Engine。

Engine 再决定：

具体使用哪个 Provider。

---

## Replaceable（可替换）

任何 Engine。

都应支持替换底层实现。

例如：

Image Engine。

今天可以使用：

GPT Image。

未来可以替换：

Flux。

Seedream。

或其它模型。

Factory 架构无需改变。

---

## Unified Interface（统一接口）

所有 Engine。

应遵循统一调用协议。

保证：

输入一致。

输出一致。

错误处理一致。

日志格式一致。

---

## Observable（可观测）

每一次 Engine 执行。

都应记录：

执行时间。

模型。

Token。

成本。

错误信息。

方便后续：

分析。

监控。

优化。

---

# 四、Engine 与 Workshop 的关系

Workshop。

负责业务。

Engine。

负责能力。

例如：

```text
Director Workshop
        │
        ▼
LLM Engine
        │
        ▼
GPT / Claude / DeepSeek
```

再例如：

```text
Asset Generation Workshop
        │
        ▼
Image Engine
        │
        ▼
GPT Image / Flux / Seedream
```

Workshop。

永远不直接调用具体模型。

统一通过 Engine。

完成能力执行。

---

# 五、Engine 分类（Engine Categories）

Factory 当前规划的核心 Engine 包括：

## Text Engine

负责：

文本生成。

剧本生成。

翻译。

总结。

分析。

---

## Image Engine

负责：

图片生成。

图片编辑。

图片优化。

---

## Video Engine

负责：

视频生成。

视频编辑。

镜头动画。

---

## Audio Engine

负责：

TTS。

背景音乐。

音效。

---

## Vision Engine

负责：

图像理解。

OCR。

视频分析。

视觉识别。

---

## Evaluation Engine

负责：

质量评分。

一致性检查。

内容审核。

自动评估。

---

## Knowledge Engine

负责：

知识检索。

向量搜索。

知识整合。

---

# 六、Engine 生命周期（Engine Lifecycle）

每次调用 Engine。

统一经历：

```text
Request

↓

Validate

↓

Execute

↓

Result

↓

Log
```

执行失败。

进入：

Retry。

Error。

Timeout。

由 Core System 统一处理。

---

# 七、标准 Engine 组成

每一个 Engine。

建议统一包含：

## Input

输入。

---

## Output

输出。

---

## Adapter

Provider 适配器。

---

## Configuration

配置。

例如：

模型。

参数。

超时。

重试。

---

## Metrics

运行指标。

包括：

耗时。

Token。

成本。

成功率。

---

## Log

完整执行日志。

---

# 八、设计原则（Design Principles）

Factory 坚持：

## Capability First

能力优先。

---

## Provider Independent

不依赖具体模型。

---

## Unified Interface

统一接口。

---

## Replaceability

支持替换。

---

## Observability

全过程可观测。

---

# 九、Non-Goals（非目标）

本章不负责：

- Prompt 编写
- Workflow 调度
- Workshop 设计
- Provider 实现
- API 细节

这些内容。

将在后续章节继续定义。

---

# 十、Dependencies（依赖关系）

Depends On：

- 500 Project Lifecycle
- 501 Workshop Architecture

Affects：

- 503 Task Scheduler
- 全部 AI Infrastructure
- 全部 Workshop

Engine Architecture。

是 Workshop 与 AI 能力之间的统一执行层。

---

# 十一、本章总结

Workshop。

决定：

谁负责。

Engine。

决定：

谁执行。

Engine Architecture。

建立了 AI Drama Factory 的统一能力执行体系。

任何 AI 服务。

任何模型。

任何 Provider。

都应通过 Engine 接入 Factory。

确保整个系统。

长期保持稳定。

可扩展。

可替换。

---

**End**