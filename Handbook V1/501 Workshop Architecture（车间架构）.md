

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

> **AI Drama Factory 应如何通过 Workshop（车间）组织整个生产系统？**

Workshop 是 Factory 的最小业务执行单元。

每一个 Workshop。

负责一项明确职责。

多个 Workshop。

共同组成完整的内容生产流水线。

Workshop 是 Factory 的核心组织方式。

也是整个 AI Drama Factory 与传统 Workflow 最大的区别。

---

# 二、设计目标（Purpose）

Workshop Architecture 的目标不是：

把所有功能放在一起。

而是：

通过多个职责清晰。

边界明确。

相互协作。

可独立演进。

的 Workshop。

构建一座真正能够持续运行的 AI Factory。

Factory 的核心不是 AI。

而是组织能力。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Single Responsibility（单一职责）

一个 Workshop。

只负责一类业务。

例如：

Director Workshop。

只负责导演。

而不是同时负责：

生图。

配音。

发布。

职责越单一。

整个 Factory 越容易维护。

---

## Standard Input / Output（标准输入输出）

所有 Workshop。

必须拥有统一的输入。

统一的输出。

禁止：

直接读取其它 Workshop 的内部数据。

所有数据交换。

必须通过统一协议完成。

---

## Independent Execution（独立执行）

每个 Workshop。

都应能够独立运行。

支持：

单独测试。

单独升级。

单独替换。

而不会影响整个 Factory。

---

## Pipeline Collaboration（流水线协作）

Workshop 之间。

并不是互相调用。

而是：

组成流水线。

每一个 Workshop。

完成自己的工作。

然后将结果交给下一站。

形成标准生产流程。

---

## Replaceability（可替换）

任何 Workshop。

理论上都可以重新实现。

例如：

Director Workshop。

可以使用：

不同 LLM。

不同 Prompt。

不同 Provider。

Factory 不应因此发生架构变化。

---

# 四、Workshop 的定义（Workshop Definition）

Workshop 是：

Factory 中负责完成某一类业务能力的独立生产单元。

每一个 Workshop。

至少包含：

- Input
- Output
- Rules
- Engine
- State
- Log

每一个 Workshop。

都拥有明确边界。

禁止承担多个业务角色。

---

# 五、Workshop 生命周期（Workshop Lifecycle）

一个 Workshop。

通常经历：

```text
Waiting

↓

Ready

↓

Running

↓

Completed

↓

Archived
```

运行失败。

可进入：

Retry。

Error。

Paused。

统一由 Core System 管理。

---

# 六、标准 Workshop 组成

每一个 Workshop。

建议统一包含：

## Input

输入数据。

---

## Output

输出结果。

---

## Engine

核心执行能力。

例如：

LLM。

Image。

Video。

TTS。

---

## Configuration

配置。

例如：

模型。

参数。

Prompt。

限制条件。

---

## State

当前状态。

例如：

Waiting。

Running。

Completed。

---

## Metrics

统计数据。

例如：

耗时。

Token。

成本。

成功率。

---

## Log

运行日志。

便于：

追踪。

排查。

分析。

---

# 七、Factory Workshop 组成

AI Drama Factory 当前规划包含：

- 600 Market Intelligence Workshop（市场情报车间）
- 601 Story Intelligence Workshop（故事分析车间）
- 602 Validation Workshop（质量筛选车间）
- 603 Director Workshop（导演车间）
- 604 Asset Generation Workshop（素材生成车间）
- 605 Video Generation Workshop（视频生成车间）
- 606 Audio Workshop（音频车间）
- 607 Subtitle Workshop（字幕车间）
- 608 Publishing Workshop（发布车间）
- 609 Analytics Workshop（数据分析车间）
- 610 Learning Workshop（学习车间）

未来。

Factory 可以继续增加新的 Workshop。

无需修改整体架构。

---

# 八、设计原则（Design Principles）

Factory 坚持：

## One Workshop One Responsibility

一个车间。

一种能力。

---

## Loose Coupling

低耦合。

---

## High Cohesion

高内聚。

---

## Standard Protocol

统一协议。

---

## Continuous Evolution

持续演进。

---

# 九、Non-Goals（非目标）

本章不负责：

- Engine 内部实现
- Prompt 设计
- AI 模型选择
- Task 调度
- Event 通信

这些内容。

将在后续章节继续定义。

---

# 十、Dependencies（依赖关系）

Depends On：

- 500 Project Lifecycle

Affects：

- 502 Engine Architecture
- 503 Task Scheduler
- 全部 600 Workshop

Workshop Architecture。

定义了整个 Factory 的组织方式。

也是所有 Workshop 章节的统一基础。

---

# 十一、本章总结

Workshop。

不是普通的软件模块。

也不是传统意义上的 Workflow。

它是 AI Drama Factory 中。

具有明确职责。

统一协议。

独立运行。

持续演进。

的业务生产单元。

多个 Workshop。

共同组成真正的 AI Factory。

---

**End**