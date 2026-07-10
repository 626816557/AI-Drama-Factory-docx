

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

> **AI Drama Factory 应如何设计、管理和维护 Prompt？**

Prompt Convention 定义整个 Factory 的 Prompt 规范。

包括：

- Prompt 设计
- Prompt 组织
- Prompt 生命周期
- Prompt 版本
- Prompt 管理

Prompt 是 AI Drama Factory 最重要的生产资产之一。

---

# 二、设计目标（Purpose）

Prompt 不只是：

发送给 AI 的一句话。

而是：

Factory 的生产规则。

优秀 Prompt 应满足：

- 可维护
- 可复用
- 可版本化
- 可测试
- 可组合
- 可演进

Prompt 应作为正式工程资产进行管理。

---

# 三、核心理念（Core Philosophy）

AI Drama Factory 坚持：

> **Prompt Is Code（Prompt 即代码）**

Prompt 与源码拥有相同的重要性。

任何 Prompt。

都应：

- 进入 Git
- 接受 Review
- 支持 Version
- 支持回滚
- 支持测试

Prompt 不属于临时文本。

而属于正式开发内容。

---

# 四、Prompt 生命周期（Lifecycle）

Factory 推荐 Prompt 生命周期如下：

```
Design

↓

Review

↓

Version

↓

Testing

↓

Production

↓

Evaluation

↓

Optimization
```

任何重要 Prompt。

都应经过完整生命周期。

---

# 五、Prompt 分类（Prompt Categories）

Factory 将 Prompt 分为以下几类。

## System Prompt

定义 AI 的长期角色。

例如：

Hollywood Director

Story Analyst

Quality Reviewer

---

## Workflow Prompt

用于某个 Workshop。

例如：

Director Prompt

Renderer Prompt

Validator Prompt

---

## Task Prompt

完成某一个具体任务。

例如：

生成角色。

生成标题。

生成封面。

---

## Evaluation Prompt

用于：

评分。

Review。

质量检查。

---

## Utility Prompt

用于：

格式转换。

翻译。

总结。

提取。

---

# 六、Prompt 组织（Organization）

Prompt 不应散落在代码中。

推荐统一管理。

例如：

```
prompts/

system/

workflow/

task/

evaluation/

shared/
```

业务代码。

通过 Prompt Loader 获取 Prompt。

不得直接硬编码。

---

# 七、Prompt 设计原则（Prompt Design）

优秀 Prompt 应满足：

- 单一目标
- 输入明确
- 输出明确
- 格式固定
- 易于测试
- 易于修改

避免：

一个 Prompt 完成多个复杂任务。

---

# 八、Prompt Version（版本管理）

每一个重要 Prompt。

应具有独立版本。

例如：

```
Director Prompt

V1

V2

V3
```

任何升级。

应记录：

修改原因。

修改内容。

影响范围。

方便回滚。

---

# 九、Prompt Review

任何核心 Prompt。

修改前。

应经过：

Review。

验证。

实验。

避免直接影响生产。

Prompt Review 与 Code Review 同等重要。

---

# 十、Prompt Testing（测试）

Prompt 应支持：

- 单元测试
- 样例测试
- Regression Test（回归测试）
- A/B Test

Prompt 修改后。

应验证：

输出质量。

一致性。

稳定性。

---

# 十一、Prompt Library

所有成熟 Prompt。

进入：

Prompt Library。

形成 Factory 长期资产。

Prompt Library 支持：

- 搜索
- 分类
- 标签
- Version
- Owner
- Change Log

---

# 十二、Prompt Security

Prompt 中不得包含：

- API Key
- Token
- Password
- Secret

Prompt 应与配置完全分离。

---

# 十三、Prompt Evolution（持续演进）

Prompt 不断优化。

但遵循：

```
Backlog

↓

Experiment

↓

Review

↓

Production
```

任何升级。

均应有明确依据。

避免凭感觉修改。

---

# 十四、设计原则（Design Principles）

Factory 坚持：

## Prompt Is Code

Prompt 是代码。

---

## Prompt Is Asset

Prompt 是资产。

---

## Prompt Is Versioned

Prompt 必须版本化。

---

## Prompt Is Testable

Prompt 必须可测试。

---

## Prompt Is Reusable

Prompt 必须可复用。

---

## Prompt Is Maintainable

Prompt 必须长期维护。

---

# 十五、Non-Goals（非目标）

本章不负责：

- AI Model Adapter（800）
- Rule Engine（Backlog）
- Prompt Library 实现细节（810）

---

# 十六、Dependencies（依赖关系）

Depends On：

- 302 Technical Architecture
- 403 Coding Convention

Affects：

- 全部 Workshop
- 全部 AI Adapter
- 全部 LLM
- 全部 Prompt Library

---

# 十七、本章总结

Prompt Convention 定义了 AI Drama Factory 的 Prompt 工程体系。

Factory 不把 Prompt 当作字符串。

而作为：

正式工程资产。

未来。

任何 Prompt。

都应：

设计。

Review。

测试。

版本管理。

持续优化。

Prompt 将成为 Factory 长期竞争力的重要组成部分。

---

**End**