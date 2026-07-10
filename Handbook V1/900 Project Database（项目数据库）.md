

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

> **AI Drama Factory 应如何统一管理整个 Factory 的 Project 数据，并建立完整的项目生命周期数据体系？**

Project Database（项目数据库）。

负责统一管理：

整个 Factory 的全部 Project Data（项目数据）。

包括：

- Project Information
- Production Status
- Workshop Progress
- Production Blueprint
- Assets Reference
- Publishing Information
- Analytics Reference

Project。

是整个 Factory 的最小业务单元（Business Unit）。

所有生产活动。

均围绕 Project 展开。

---

# 二、Project Database 定位（Position）

Project Database。

不是：

SQLite 文件。

也不是：

某一个数据库实例。

Project Database。

是整个 Factory 的 Project Data Layer（项目数据层）。

负责：

统一存储。

统一组织。

统一管理。

全部 Project 数据。

数据库。

只是：

Project Data 的一种实现方式。

---

# 三、设计目标（Purpose）

Project Database 的目标不是：

保存数据。

而是：

建立统一。

可靠。

可追溯。

可扩展。

可持续演进。

的 Project Data Management System。

保证每一个 Project。

都拥有完整的数据生命周期。

---

# 四、Project 生命周期（Project Lifecycle）

Factory 推荐统一生命周期：

Project Created

↓

Planning

↓

Production

↓

Publishing

↓

Analytics

↓

Archived

所有 Project。

均应完整记录生命周期。

---

# 五、核心数据（Core Data）

Project Database 应统一管理：

## Project Metadata

项目基础信息。

---

## Business Information

商业信息。

---

## Workshop Status

各车间执行状态。

---

## Production Progress

生产进度。

---

## Asset References

素材引用关系。

---

## Publishing Records

发布记录。

---

## Analytics References

数据分析引用。

---

# 六、核心职责（Responsibilities）

Project Database 负责：

## Data Storage

统一存储：

Project Data。

---

## Lifecycle Management

统一管理：

Project 生命周期。

---

## Relationship Management

统一维护：

Project 与：

Story。

Character。

Asset。

Video。

Analytics。

之间的数据关系。

---

## Query Support

支持：

快速查询。

快速检索。

统一索引。

---

## Traceability

保证：

每一个 Project。

均可完整追溯。

---

# 七、设计原则（Design Principles）

Factory 坚持：

## Project First

Project。

是 Factory 的核心业务对象。

---

## Lifecycle Driven

围绕生命周期组织数据。

---

## Traceability

全过程可追溯。

---

## Data Consistency

保持数据一致性。

---

## Scalability

支持长期扩展。

---

# 八、Non-Goals（非目标）

本章不负责：

- Story Database
- Asset Storage
- Analytics Storage
- Database Engine

这些能力。

将在其它章节定义。

---

# 九、Dependencies（依赖关系）

Depends On：

- 500 Project Lifecycle
- 507 Storage System

Affects：

- 全部 Workshop
- 全部 Production Pipeline
- 全部 Business Process

Project Database。

负责整个 Factory 的 Project Data。

---

# 十、本章总结

Project Database。

不是：

数据库文件。

也不是：

SQLite。

它负责：

整个 Factory 的 Project Data Layer。

帮助 Factory。

统一管理。

统一追踪。

统一组织。

全部 Project 数据。

确保每一个 Project。

都拥有完整。

可追溯。

可持续演进。

的数据生命周期。

---

**End**