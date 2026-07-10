

> Version：V1.0
>
> Status：Draft
>
> Last Update：2026-07-07
>
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？（Purpose）

本文档回答一个问题：

> AI Drama Factory 的整体架构是什么？

Factory 不是一个脚本。

也不是多个独立工具。

它是一个长期演进的软件系统。

本文档定义整个 Factory 的分层架构、模块职责以及数据流向。

所有后续设计都必须遵循本章。

---

# 二、总体架构（Overall Architecture）

AI Drama Factory 采用分层架构（Layered Architecture）。

整体结构如下：

```text
Business（商业）

↓

Content Strategy（内容战略）

↓

Core System（核心系统）

↓

AI Production（AI 生产）

↓

Operations（运营）

↓

Infrastructure（基础设施）
```

Business 决定 Factory 为什么存在。

Content Strategy 决定 Factory 生产什么。

Core System 决定 Factory 如何运行。

AI Production 完成实际生产。

Operations 完成商业运营。

Infrastructure 提供底层运行环境。

---

# 三、软件架构（Software Architecture）

对应到实际软件系统：

```text
ADF-OS

│

├── Foundation（基础层）

├── Persistence（持久化层）

├── Kernel（内核）

├── Centers（中心层）

├── Workshops（生产车间）

├── Operations（运营层）

└── External Providers（外部服务）
```

所有代码都属于以上七层之一。

禁止跨层混乱调用。

---

# 四、Foundation（基础层）

Foundation 提供最基础能力。

特点：

- 无业务逻辑
- 高复用
- 高稳定
- 最少依赖

当前模块包括：

- Config（配置中心）
- Environment（环境管理）
- Logger（日志系统）
- Errors（异常体系）
- Utils（公共工具）

Foundation 是整个 Factory 的地基。

---

# 五、Persistence（持久化层）

Persistence 负责长期数据存储。

包括：

- Database（数据库）
- Storage（文件存储）
- Cache（缓存，未来）
- Object Storage（对象存储，未来）

Persistence 不关心业务。

只负责：

保存。

读取。

更新。

删除。

---

# 六、Kernel（内核）

Kernel 是 Factory 的调度中心。

负责：

Project 生命周期。

Workflow 调度。

Task 管理。

事件分发。

模块协调。

Kernel 不直接生产内容。

它负责组织生产。

---

# 七、Centers（中心层）

Centers 是 Factory 的管理中心。

每个 Center 负责一个领域。

例如：

AI Center

Prompt Center

Quality Center

Asset Center

Knowledge Center

Provider Center

Centers 管理资源。

Workshops 消费资源。

---

# 八、Workshops（生产车间）

Workshop 是真正执行 AI 生产的地方。

例如：

Spider Workshop

Research Workshop

Planning Workshop

Director Workshop

Image Workshop

Video Workshop

Audio Workshop

Publisher Workshop

每个 Workshop：

只负责一件事情。

执行完成后立即返回。

长期状态交给 Core System 管理。

---

# 九、Operations（运营层）

Operations 面向商业运营。

包括：

平台发布。

账号矩阵。

数据分析。

收益统计。

广告。

增长。

Operations 不参与生产。

负责 Factory 的商业闭环。

---

# 十、External Providers（外部服务）

Factory 不直接实现所有能力。

大量能力来自外部 Provider。

例如：

LLM

Image Model

Video Model

TTS

Payment

Cloud Storage

Map API

Social Media API

Provider 可以自由替换。

Factory 不应依赖具体厂商。

---

# 十一、数据流（Data Flow）

Factory 的典型运行流程：

```text
Project

↓

Workflow

↓

Kernel

↓

Workshop

↓

Asset

↓

Quality

↓

Publishing

↓

Analytics

↓

Learning

↓

Optimization
```

所有数据最终都回到 Core System。

形成持续学习闭环。

---

# 十二、模块依赖原则（Dependency Rules）

整个系统遵循单向依赖：

```text
Foundation

↓

Persistence

↓

Kernel

↓

Centers

↓

Workshops

↓

Operations
```

下层不能依赖上层。

例如：

Foundation 不能调用 Workshop。

Persistence 不能调用 Operations。

Kernel 不依赖具体 Provider。

这样可以保持架构稳定。

---

# 十三、当前开发状态（Current Status）

截至 M2：

已完成：

Foundation（基础层）

- Config
- Environment
- Logger
- Errors

Persistence（持久化层）

- Storage
- Database

下一阶段：

开始设计：

Kernel。

Centers。

Data Model。

Workflow Engine。

未来所有新增代码都必须放入正确层级。

禁止出现职责不清的新模块。

---

# 十四、本章总结（Summary）

Factory Architecture 是 AI Drama Factory 的总蓝图。

它定义：

系统如何分层。

模块如何协作。

数据如何流动。

未来如何扩展。

随着 M2 推进。

所有代码都将逐步映射到本架构。

未来无论增加新的 AI 模型、生产车间还是运营能力，都不应破坏本章定义的整体结构。

---

**End**