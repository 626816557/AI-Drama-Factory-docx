

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

> **AI Drama Factory 应如何使用 Git 管理整个项目？**

Git Convention 定义项目统一的版本管理规范。

包括：

- 分支管理
- 提交原则
- 合并原则
- 版本管理
- 发布流程

Git 是整个 Factory 的历史记录。

也是所有设计演进的重要依据。

---

# 二、设计目标（Purpose）

Git 的目标不仅是保存代码。

更重要的是：

- 保存历史
- 保存设计
- 保存决策
- 保存演进过程

未来。

任何版本。

都应能够追溯。

---

# 三、核心原则（Core Principles）

Factory 遵循以下 Git 原则。

## Git Is History

Git 保存的不只是代码。

而是整个 Factory 的成长历史。

---

## Small Changes

保持小步提交。

避免：

一次 Commit 修改整个系统。

每次提交。

都应完成一个完整目标。

---

## Atomic Commit

一次 Commit。

只解决一个问题。

例如：

修复 Bug。

新增 Workshop。

调整 Prompt。

不要混合多个目的。

---

## Traceable

任何 Commit。

都应能够回答：

为什么修改？

修改了什么？

影响哪些模块？

---

## Stable Main

main 分支。

始终保持可运行状态。

任何实验。

不得直接进入 main。

---

# 四、分支策略（Branch Strategy）

Factory 推荐：

```
main

↓

feature/*

↓

release/*

↓

hotfix/*
```

各分支职责明确。

避免长期混乱。

---

# 五、开发流程（Workflow）

推荐流程：

```
main

↓

feature

↓

Review

↓

Merge

↓

Release
```

任何功能。

完成 Review 后。

再合并。

---

# 六、提交原则（Commit Principle）

每次 Commit 应满足：

- 可以独立理解
- 可以独立回滚
- 可以独立 Review

禁止：

大量无意义提交。

例如：

```
update

fix

test

123
```

---

# 七、版本管理（Version Management）

Factory 使用：

Semantic Versioning。

例如：

```
V1.0.0

V1.1.0

V1.1.1
```

Major：

重大升级。

Minor：

新增功能。

Patch：

Bug 修复。

---

# 八、冲突处理（Conflict）

发生 Merge Conflict 时。

优先：

理解设计。

而不是：

快速解决。

任何冲突。

都应保证：

Handbook 与代码保持一致。

---

# 九、回滚原则（Rollback）

任何版本。

都应支持：

快速回滚。

禁止：

通过覆盖代码解决问题。

Git History 应保持完整。

---

# 十、Tag 管理（Tag）

重要版本。

建议创建 Tag。

例如：

```
V1.0

V1.1

V2.0
```

Tag 用于记录重要里程碑。

方便长期维护。

---

# 十一、设计原则（Design Principles）

Factory 坚持：

## History First

历史不可丢失。

---

## Review Before Merge

合并前完成 Review。

---

## Stable Main

主分支始终稳定。

---

## Recoverability

任何版本可恢复。

---

## Documentation Consistency

Git 历史应与 Handbook 保持一致。

---

# 十二、Non-Goals（非目标）

本章不负责：

- Branch 命名规范（405）
- Commit Message（406）
- Release 规范（413）

---

# 十三、Dependencies（依赖关系）

Depends On：

- 400 Project Convention

Affects：

- 全部源码
- 全部文档
- 全部开发流程

---

# 十四、本章总结

Git Convention 定义了 AI Drama Factory 的版本管理方式。

Git 不是代码备份工具。

而是整个 Factory 的历史系统。

未来。

任何修改。

任何设计。

任何演进。

都应通过统一 Git 流程完成。

---

**End**