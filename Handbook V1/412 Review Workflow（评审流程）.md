

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

> **AI Drama Factory 应如何开展统一的 Review（评审）工作？**

Review Workflow 定义整个 Factory 的评审体系。

包括：

- Handbook Review
- Architecture Review
- Prompt Review
- Code Review
- AI Output Review
- Release Review

Review 是 Factory 质量保障的重要组成部分。

---

# 二、设计目标（Purpose）

Review 的目标不是：

寻找错误。

而是：

保证质量。

统一标准。

降低风险。

持续优化。

Review 应帮助整个 Factory 持续成长。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Review Is Improvement

Review 的目的。

是帮助改进。

而不是否定开发者。

---

## Fact Based

所有 Review。

应基于：

事实。

数据。

规范。

避免：

主观判断。

---

## Handbook Driven

Review 的依据。

首先是 Handbook。

而不是个人习惯。

当出现争议时。

优先参考正式规范。

---

## Quality First

任何功能。

在质量未达标前。

不得进入正式版本。

---

## Continuous Learning

Review 发现的问题。

应沉淀经验。

必要时进入：

Backlog。

Handbook。

Knowledge Base。

---

# 四、Review 分类（Review Categories）

Factory 定义六类 Review。

---

## Handbook Review

评审：

设计是否完整。

是否合理。

是否符合整体架构。

---

## Architecture Review

评审：

新增设计。

是否影响整体系统。

是否符合架构原则。

---

## Prompt Review

评审：

Prompt：

是否稳定。

是否可维护。

是否可复用。

是否符合 Prompt Convention。

---

## Code Review

评审：

代码质量。

规范一致性。

可维护性。

是否符合 Handbook。

---

## AI Output Review

评审：

AI 生成结果。

例如：

剧本。

图片。

视频。

字幕。

是否符合质量标准。

---

## Release Review

正式发布前。

确认：

所有质量要求均已满足。

---

# 五、统一 Review 流程

所有 Review。

遵循统一流程：

```
Submit

↓

Check

↓

Feedback

↓

Revision

↓

Approval

↓

Archive
```

Review 完成后。

保留历史记录。

支持追溯。

---

# 六、Review 检查维度

Review 至少包含以下维度：

## Design

是否符合整体设计？

---

## Convention

是否符合项目规范？

---

## Quality

质量是否达标？

---

## Maintainability

未来是否容易维护？

---

## Scalability

未来是否容易扩展？

---

## Consistency

是否保持整体一致？

---

# 七、Review 输出

每一次 Review。

至少产生：

- Review Result
- Review Comment
- Decision
- Reviewer
- Time

保证所有评审均可追踪。

---

# 八、Review 决策

Review 结果统一分为：

```
Approved

Approved with Changes

Needs Revision

Rejected
```

所有结论。

应有明确原因。

---

# 九、AI 在 Review 中的角色

AI 可以协助：

- 检查规范
- 检查命名
- 检查重复代码
- 检查 Prompt
- 检查文档一致性

但：

最终 Review 结论。

仍由人工负责确认。

---

# 十、Review 设计原则（Design Principles）

Factory 坚持：

## Objective Review

客观评审。

---

## Handbook First

规范优先。

---

## Continuous Improvement

持续优化。

---

## Traceable

全过程可追溯。

---

## Respectful Collaboration

尊重事实。

尊重设计。

尊重他人。

---

# 十一、Non-Goals（非目标）

本章不负责：

- Git Review 工具
- Pull Request 平台
- 自动化 CI 配置

---

# 十二、Dependencies（依赖关系）

Depends On：

- 400 Project Convention
- 403 Coding Convention
- 407 Prompt Convention

Affects：

- 全部 Handbook
- 全部代码
- 全部 Prompt
- 全部 Workshop
- 全部 AI 输出

---

# 十三、本章总结

Review Workflow 定义了 AI Drama Factory 的统一评审体系。

Factory 不依赖：

个人经验。

个人喜好。

而依赖：

统一标准。

统一规范。

统一质量要求。

未来。

任何设计。

任何代码。

任何 Prompt。

任何 AI 输出。

都应经过统一 Review。

---

**End**