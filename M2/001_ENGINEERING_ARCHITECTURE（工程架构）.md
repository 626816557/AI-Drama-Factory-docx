

> Version：V1.0
>
> Status：Draft
>
> Milestone：M2
>
> Last Update：2026-07-07
>
> Owner：AI Drama Factory

---

# 一、文档目的（Purpose）

本文档定义 AI Drama Factory 的整体工程架构（Engineering Architecture）。

它回答以下几个核心问题：

- Factory 的工程应该如何组织？
- 每个目录承担什么职责？
- 模块之间如何协作？
- 如何保证未来长期可维护性？
- 如何支持未来持续扩展新的能力？

本规范是整个 M2 的第一份工程设计文档，也是所有后续开发工作的基础。

---

# 二、设计目标（Design Goals）

AI Drama Factory 不是一个普通的 Node.js 项目，而是一个长期演进的 AI 内容生产系统。

因此，工程架构必须满足以下目标：

- 可维护性（Maintainability）
- 可扩展性（Scalability）
- 模块化（Modularity）
- 高内聚（High Cohesion）
- 低耦合（Low Coupling）
- 长期稳定（Long-term Stability）

任何新的模块，都必须遵循本规范。

---

# 三、核心设计原则（Core Design Principles）

整个工程遵循以下原则。

## 3.1 Handbook First（Handbook 优先）

Handbook 是最高设计文档。

所有工程实现必须遵循 Handbook，而不是反过来根据代码修改 Handbook。

---

## 3.2 Responsibility First（职责优先）

目录不是按照文件类型划分。

而是按照职责（Responsibility）划分。

每一个目录都必须有明确且唯一的职责。

避免出现职责交叉。

---

## 3.3 Single Responsibility（单一职责）

每一个模块只负责一件事情。

例如：

Logger（日志）只负责日志。

Database（数据库）只负责数据持久化。

Workflow（工作流）只负责流程调度。

任何模块都不应该承担多个职责。

---

## 3.4 Layered Architecture（分层架构）

Factory 采用严格的分层设计。

每一层拥有明确边界。

上层依赖下层。

下层不能反向依赖上层。

禁止跨层调用。

---

## 3.5 Protocol First（协议优先）

任何模块之间的数据交换，都必须先定义 Protocol（协议）。

模块之间禁止直接依赖内部实现。

这样才能保证未来自由替换实现。

---

## 3.6 Model Agnostic（模型无关）

任何 AI Provider（AI 服务提供商）都只是 Factory 的一种实现。

Factory 永远不能绑定某一个模型。

GPT、Claude、Gemini、DeepSeek 等都应该可以自由替换。

---

# 四、整体架构（Overall Architecture）

AI Drama Factory 采用五层架构（Five-Layer Architecture）。

```

Foundation（基础层）

↓

Kernel（内核）

↓

Centers（中心层）

↓

Workshops（生产车间）

↓

Operations（运营层）

```

每一层都有独立职责。

任何新能力都必须归属于其中一层。

---

# 五、各层职责（Layer Responsibilities）

## Foundation（基础层）

Foundation 提供整个 Factory 的基础能力。

例如：

- Configuration（配置）
- Logging（日志）
- Database（数据库）
- Storage（存储）
- Environment（环境）
- Error Handling（异常处理）
- Utilities（公共工具）

Foundation 不包含任何业务逻辑。

---

## Kernel（内核）

Kernel 是整个 Factory 的核心。

负责协调所有模块。

未来包括：

- Workflow Engine（工作流引擎）
- Task Scheduler（任务调度器）
- Project Manager（项目管理器）
- Resource Manager（资源管理器）
- Capability Registry（能力注册中心）

Kernel 不直接生产内容。

它只负责组织生产。

---

## Centers（中心层）

Centers 保存 Factory 的长期资产。

例如：

- Knowledge Center（知识中心）
- Asset Center（资产中心）
- Configuration Center（配置中心）
- Evaluation Center（评估中心）

Centers 不负责执行生产任务。

而负责管理 Factory 的知识与资源。

---

## Workshops（生产车间）

Workshops 是真正的生产模块。

例如：

- Market Workshop（市场车间）
- Story Workshop（故事车间）
- Director Workshop（导演车间）
- Image Workshop（图片车间）
- Video Workshop（视频车间）
- Audio Workshop（音频车间）
- Publishing Workshop（发布车间）

所有业务能力最终都属于 Workshop。

---

## Operations（运营层）

Operations 面向商业运营。

例如：

- Analytics（数据分析）
- ROI Analysis（ROI 分析）
- Account Matrix（账号矩阵）
- Growth（增长）
- A/B Testing（A/B 测试）

Operations 不参与生产。

负责持续优化 Factory 的商业表现。

---

# 六、依赖原则（Dependency Rules）

整个 Factory 遵循单向依赖原则。

```

Operations

↓

Workshops

↓

Centers

↓

Kernel

↓

Foundation

```

任何模块不得违反依赖方向。

例如：

Foundation 不允许调用 Workshop。

Workshop 不允许直接操作 Foundation 内部实现。

所有调用必须通过公开接口完成。

---

# 七、本章总结（Summary）

Engineering Architecture（工程架构）是 AI Drama Factory 的第一份工程规范。

从 M2 开始，所有新增模块都必须遵循本规范。

未来，无论增加多少 Workshop、多少 AI Provider、多少商业能力，整个 Factory 都必须保持统一的工程架构。

本规范将作为后续所有 Engineering Specification（工程设计规范）的基础。

---

**End**