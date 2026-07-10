

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

> **AI Drama Factory 应如何判断一个 Project 是否值得进入正式生产？**

Validation Workshop（质量筛选车间）。

负责整个 Factory 的生产准入（Production Validation）。

它决定：

哪些 Project。

值得投入 Factory 资源。

哪些 Project。

应当终止。

Validation。

不是为了评价故事。

而是为了：

做出生产决策。

---

# 二、Workshop 定位（Workshop Position）

Validation Workshop。

位于：

Story Intelligence Workshop。

之后。

Director Workshop。

之前。

它负责回答：

> **这个 Project 是否值得正式生产？**

而不是：

> **故事写得好不好？**

Factory。

不是所有 Story。

都会生产。

只有通过 Validation。

才能正式进入 Factory。

---

# 三、设计目标（Purpose）

Validation Workshop 的目标不是：

寻找最好的故事。

而是：

寻找最值得生产的 Project。

Validation 的核心。

不是评分。

而是：

Production Decision（生产决策）。

---

# 四、输入（Input）

Validation Workshop。

输入：

- Market Intelligence
- Story Intelligence
- Business Strategy
- Factory Policy
- Historical Performance（可选）

所有输入。

统一称为：

Production Candidate。

---

# 五、输出（Output）

Validation Workshop。

输出：

Production Decision。

包括：

- PASS
- REJECT
- HOLD（可选）

同时输出：

Validation Report。

记录：

通过原因。

拒绝原因。

风险说明。

推荐建议。

---

# 六、核心职责（Responsibilities）

Validation Workshop。

负责：

## Commercial Validation（商业验证）

判断：

是否具有商业价值。

---

## Production Validation（生产验证）

判断：

是否值得投入 Factory 资源。

---

## Risk Validation（风险验证）

识别：

潜在风险。

包括：

政策。

版权。

生产成本。

市场风险。

---

## ROI Evaluation（收益评估）

预估：

投入。

收益。

ROI。

帮助 Factory 做出生产决策。

---

## Production Decision（生产决策）

最终输出：

PASS。

REJECT。

或：

HOLD。

进入下一阶段。

---

# 七、标准流程（Workflow）

Factory 推荐统一流程：

```text
Receive Production Candidate

↓

Business Evaluation

↓

Production Evaluation

↓

Risk Evaluation

↓

ROI Evaluation

↓

Production Decision

↓

Output
```

Validation。

不是生产。

而是：

决定是否生产。

---

# 八、上下游关系（Upstream & Downstream）

上游：

601 Story Intelligence Workshop。

下游：

603 Director Workshop。

Validation。

连接：

故事分析。

与。

正式生产。

它是 Factory 的立项决策中心。

---

# 九、设计原则（Design Principles）

Factory 坚持：

## Business First

商业价值优先。

---

## Resource Awareness

合理使用 Factory 资源。

---

## Risk Control

风险控制。

---

## Objective Evaluation

客观评估。

---

## Production Decision

统一立项。

---

# 十、Non-Goals（非目标）

本章不负责：

- 剧本创作
- Prompt 编写
- Director
- Asset Generation
- Video Generation
- 图片质量评价

这些能力。

将在后续 Workshop 中完成。

---

# 十一、Dependencies（依赖关系）

Depends On：

- 600 Market Intelligence Workshop
- 601 Story Intelligence Workshop

Affects：

- 603 Director Workshop
- 全部 Production Pipeline

Validation Workshop。

决定 Factory 是否正式启动生产。

---

# 十二、本章总结

Validation Workshop。

不是：

内容评分器。

也不是：

图片质量检查。

它负责：

Production Validation（生产准入验证）。

帮助 Factory。

在投入生产资源之前。

完成统一立项。

只有通过 Validation。

Project 才能正式进入：

Director Workshop。

---

**End**