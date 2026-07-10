

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

> **AI Drama Factory 应遵循什么样的数据库设计规范？**

Database Convention 定义整个项目的数据库开发规范。

包括：

- 数据模型
- 表设计
- 字段设计
- Migration
- Version
- 数据一致性

本章不定义业务数据。

业务模型由：

303 Data Architecture

负责。

---

# 二、设计目标（Purpose）

数据库不仅用于保存数据。

更应保证：

- 一致性
- 可维护性
- 可扩展性
- 可迁移性
- 可恢复性

数据库属于长期资产。

设计必须稳定。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Data First

数据库首先服务于数据模型。

而不是代码实现。

---

## Consistency

所有表。

所有字段。

保持统一规范。

---

## Backward Compatibility

数据库升级。

优先保证兼容。

避免破坏已有数据。

---

## Migration First

任何数据库修改。

必须通过 Migration。

禁止：

直接修改线上数据库。

---

## Traceability

任何数据变化。

应能够追溯来源。

---

# 四、数据库选型（Database Selection）

V1 推荐：

```
PostgreSQL
```

作为主数据库。

原因：

- 开源
- 稳定
- 功能丰富
- JSON 支持优秀
- 扩展能力强

未来如需新增数据库。

不得影响现有数据模型。

---

# 五、表设计（Table Design）

所有表：

统一采用：

```
snake_case
```

例如：

```
projects

story_scripts

character_profiles

video_assets

publish_records
```

表名使用复数形式。

保持统一。

---

# 六、字段设计（Column Design）

字段统一采用：

```
snake_case
```

例如：

```
project_id

created_at

updated_at

deleted_at

status
```

字段名称应表达真实含义。

避免缩写。

---

# 七、主键设计（Primary Key）

所有业务实体。

统一采用：

```
id
```

作为主键字段。

具体 ID 类型由实现决定（如 UUID、雪花 ID、自增等）。

Factory 不强制绑定具体实现。

但要求：

- 全局唯一
- 长期稳定
- 不可复用

---

# 八、时间字段（Timestamp）

所有主要业务表。

统一包含：

```
created_at

updated_at
```

根据业务需要。

可增加：

```
deleted_at
```

支持软删除。

保持历史完整。

---

# 九、删除策略（Delete Policy）

默认：

采用：

```
Soft Delete
```

重要数据。

原则上不直接物理删除。

例如：

- Project
- IP
- Character
- Asset

真正删除。

应经过明确确认。

---

# 十、Migration（数据库迁移）

所有数据库结构修改。

必须通过 Migration。

Migration 应满足：

- 可执行
- 可回滚（如适用）
- 可重复验证
- 可追踪

禁止：

手工修改正式数据库结构。

---

# 十一、索引设计（Index）

索引应根据：

查询模式。

业务需求。

性能分析。

进行设计。

避免：

无意义索引。

重复索引。

过度索引。

索引属于性能优化。

不是默认配置。

---

# 十二、事务（Transaction）

涉及多个数据修改时。

应使用事务。

保证：

全部成功。

或全部失败。

避免：

部分成功。

部分失败。

导致数据不一致。

---

# 十三、数据完整性（Integrity）

数据库应保证：

- 主键完整
- 外键一致（根据具体架构选择是否使用数据库外键）
- 数据合法
- 状态正确

任何非法数据。

应尽可能在进入数据库之前被拦截。

---

# 十四、版本管理（Version）

数据库 Schema。

应具有版本。

所有 Migration。

均应记录：

- 时间
- 作者
- 原因
- 影响范围

保证数据库长期可维护。

---

# 十五、设计原则（Design Principles）

Factory 坚持：

## Stable Schema

Schema 保持稳定。

---

## Migration Driven

所有变更通过 Migration。

---

## Data Integrity

保证数据一致性。

---

## Long-term Compatibility

优先兼容已有数据。

---

## Recoverability

数据库支持恢复。

---

# 十六、Non-Goals（非目标）

本章不负责：

- Data Architecture（303）
- Repository 实现
- ORM 选型
- SQL 优化细节

---

# 十七、Dependencies（依赖关系）

Depends On：

- 303 Data Architecture
- 302 Technical Architecture

Affects：

- Backend
- Repository
- Migration
- Analytics
- Knowledge

---

# 十八、本章总结

Database Convention 定义了 AI Drama Factory 的数据库开发规范。

数据库不是代码附属品。

而是整个 Factory 的长期数据资产。

未来。

任何数据结构。

任何 Migration。

任何数据库升级。

都应遵循统一数据库规范。

---

**End**