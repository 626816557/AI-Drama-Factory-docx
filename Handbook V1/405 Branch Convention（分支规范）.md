

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

> **AI Drama Factory 应如何设计和管理 Git Branch（分支）？**

Branch Convention 定义整个项目的分支策略。

包括：

- 分支职责
- 生命周期
- 合并规则
- 删除规则

所有开发工作。

均应基于统一 Branch Strategy。

---

# 二、设计目标（Purpose）

Branch 的目标不是：

同时存在很多代码。

而是：

让不同开发任务能够安全并行。

同时保证：

- Main 始终稳定
- Feature 相互隔离
- Release 可追踪
- Bug 可快速修复

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Main Always Stable

main 分支。

始终保持：

可运行。

可发布。

可演示。

任何未完成开发。

不得直接进入 main。

---

## One Feature One Branch

一个功能。

一个 Branch。

禁止：

一个 Branch 开发多个功能。

---

## Short-lived Branch

Feature Branch 应保持生命周期尽可能短。

开发完成后。

及时：

Review。

Merge。

Delete。

避免长期存在。

---

## Branch Has Responsibility

每一个 Branch。

都应拥有唯一职责。

禁止：

万能 Branch。

长期开发 Branch。

---

# 四、标准分支

Factory 定义以下标准分支。

---

## main

正式版本。

唯一长期存在分支。

特点：

- 可运行
- 可部署
- 可发布

任何时候。

main 都代表 Factory 当前稳定版本。

---

## feature/*

用于：

新功能开发。

例如：

```
feature/director-workshop

feature/adf-dashboard

feature/video-center
```

开发完成后。

合并进入 main。

随后删除。

---

## release/*

用于：

发布准备。

例如：

```
release/v1.0

release/v1.1
```

负责：

最终测试。

Bug 修复。

发布确认。

发布完成后。

删除。

---

## hotfix/*

用于：

紧急修复。

例如：

```
hotfix/login-bug

hotfix/render-timeout
```

修复完成后。

立即合并回 main。

随后删除。

---

# 五、Branch 生命周期

Feature：

```
Create

↓

Development

↓

Review

↓

Merge

↓

Delete
```

任何 Feature。

不应长期存在。

---

# 六、Merge 原则（Merge Policy）

Merge 前必须确认：

✓ 功能完成

✓ Handbook 已同步

✓ Review 完成

✓ 测试通过

满足以上条件。

方可进入 main。

---

# 七、Branch 命名

统一使用：

```
feature/

release/

hotfix/
```

后接：

```
kebab-case
```

例如：

```
feature/story-workshop

feature/project-center

hotfix/video-export

release/v1.0
```

禁止：

```
new

temp

test

abc

my-branch
```

---

# 八、Branch 删除

Merge 完成后。

及时删除：

Feature。

Release。

Hotfix。

保持仓库整洁。

长期保留：

```
main
```

---

# 九、禁止行为

禁止：

直接在：

```
main
```

开发。

---

禁止：

长期存在：

```
feature-old

test-final

backup

```

---

禁止：

多个功能共享一个 Feature Branch。

---

# 十、设计原则（Design Principles）

Factory 坚持：

## Stable Main

主分支稳定。

---

## Independent Feature

功能独立。

---

## Fast Merge

及时合并。

---

## Clear History

保持清晰历史。

---

## Easy Rollback

方便快速恢复。

---

# 十一、Non-Goals（非目标）

本章不负责：

- Commit Message（406）
- Release 流程（413）
- Git 工具使用

---

# 十二、Dependencies（依赖关系）

Depends On：

- 404 Git Convention

Affects：

- 全部开发流程
- 全部代码管理
- 全部版本发布

---

# 十三、本章总结

Branch Convention 定义了 AI Drama Factory 的分支策略。

每一个 Branch。

都应拥有明确职责。

保持：

简单。

稳定。

短生命周期。

未来。

整个 Factory 应始终保持：

Main 可发布。

Feature 可开发。

Release 可验证。

Hotfix 可快速修复。

---

**End**