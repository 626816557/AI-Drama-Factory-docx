# AI Drama Factory

# 002 Foundation Dependency Design（基础层依赖设计）

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

本文档定义 Foundation（基础层）内部各模块之间的依赖关系。

Foundation（基础层）是 AI Drama Factory 的最低层能力，负责为 Kernel（内核）、Centers（中心层）、Workshops（生产车间）和 Operations（运营层）提供稳定的基础服务。

本文档只回答一个问题：

> Foundation 内部模块应该如何依赖，才能长期稳定、清晰、可扩展？

---

# 二、Foundation 模块范围（Module Scope）

当前 Foundation（基础层）包含以下模块：

- Config（配置中心）
- Environment（环境管理）
- Logger（日志系统）
- Errors（异常体系）
- Events（事件总线）
- Storage（存储系统）
- Database（数据库）
- Utils（公共工具）

这些模块必须保持职责清晰，避免相互循环依赖。

---

# 三、核心原则（Core Principles）

## 3.1 Config First（配置优先）

Config（配置中心）是 Foundation 的第一个模块。其它模块可以读取配置，但 Config 不能依赖其它 Foundation 模块。

例如，Logger 可以读取 `logging.level`，Database 可以读取 `database.path`，Storage 可以读取 `paths.workspace`。

## 3.2 No Circular Dependency（禁止循环依赖）

Foundation 内部禁止出现循环依赖。

例如：

```text
Logger → Events → Logger