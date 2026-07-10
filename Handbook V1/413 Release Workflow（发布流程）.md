

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

> **AI Drama Factory 应如何完成一次正式的软件发布？**

Release Workflow 定义整个 Factory 的发布流程。

包括：

- 发布准备
- 最终验证
- 正式发布
- 发布确认
- 发布回滚
- 发布总结

Release 是 Factory 生命周期的重要节点。

任何正式版本。

都应遵循统一流程。

---

# 二、设计目标（Purpose）

Release Workflow 的目标不是：

快速上线。

而是：

稳定上线。

可恢复。

可追溯。

可持续迭代。

每一次发布。

都应成为 Factory 的一个正式里程碑。

---

# 三、核心原则（Core Principles）

Factory 坚持：

## Quality Before Release

质量优先。

而不是发布时间优先。

任何未达到质量要求的版本。

不得发布。

---

## Handbook Consistency

正式发布前。

Handbook。

代码。

文档。

必须保持一致。

---

## Traceable Release

每一次 Release。

都必须能够回答：

为什么发布？

修改了什么？

影响哪些模块？

如何恢复？

---

## Recoverable Release

任何发布。

都应支持快速回滚。

避免：

不可恢复的发布。

---

## Continuous Delivery

发布不是终点。

而是：

下一轮持续优化的开始。

---

# 四、标准发布流程（Release Workflow）

Factory 推荐统一流程：

```
Feature Freeze

↓

Testing

↓

Review

↓

Release Candidate（RC）

↓

Final Validation

↓

Release

↓

Monitoring

↓

Retrospective
```

---

# 五、阶段说明

## 1、Feature Freeze

停止新增功能。

只允许：

Bug 修复。

文档完善。

版本整理。

保证发布范围稳定。

---

## 2、Testing

完成：

- Unit Test
- Integration Test
- End-to-End Test
- Manual Validation（必要时）

确保版本符合设计预期。

---

## 3、Release Review

确认：

- Handbook 已同步
- Code Review 完成
- Prompt Review 完成
- 测试通过
- Change Log 完整

通过后。

进入 RC。

---

## 4、Release Candidate（RC）

生成候选版本。

例如：

```
V1.0.0-RC1

V1.0.0-RC2
```

RC 用于最终验证。

原则上。

不再新增功能。

---

## 5、Final Validation

最终检查：

- 功能完整性
- 数据一致性
- 配置正确性
- 部署环境
- AI 服务状态

确认满足发布条件。

---

## 6、Release

正式发布。

包括：

- Git Tag
- Version 更新
- Change Log
- Handbook Version
- Deployment

形成正式版本。

---

## 7、Monitoring

发布完成后。

持续监控：

- API 状态
- Workshop 状态
- AI 调用
- GPU
- 日志
- 用户反馈

及时发现问题。

---

## 8、Retrospective

发布结束后。

总结：

成功经验。

存在问题。

改进建议。

需要优化的内容。

统一进入：

Backlog。

等待下一轮演进。

---

# 六、发布检查清单（Release Checklist）

正式发布前。

至少确认：

✓ Handbook 已 Freeze

✓ Architecture 无冲突

✓ Code Review 完成

✓ Prompt Review 完成

✓ 测试通过

✓ Migration 已验证

✓ Version 已更新

✓ Change Log 已完成

✓ Deployment 已验证

---

# 七、版本管理（Release Version）

正式版本。

统一采用：

Semantic Versioning。

例如：

```
V1.0.0

V1.1.0

V1.1.1
```

所有版本。

均应建立：

Git Tag。

便于长期维护。

---

# 八、回滚策略（Rollback）

任何正式发布。

均应支持：

- 快速回滚
- 数据恢复
- 配置恢复
- Prompt 恢复
- Handbook 对应版本恢复

回滚过程。

应有明确记录。

---

# 九、发布产物（Release Deliverables）

每次 Release。

至少产生：

- Git Tag
- Release Note
- Change Log
- Handbook Version
- Deployment Record

所有发布产物。

统一进入版本管理。

---

# 十、设计原则（Design Principles）

Factory 坚持：

## Stable Release

稳定优先。

---

## Recoverability

支持恢复。

---

## Traceability

全过程可追溯。

---

## Documentation Consistency

文档与代码一致。

---

## Continuous Improvement

持续发布。

持续优化。

---

# 十一、Non-Goals（非目标）

本章不负责：

- CI/CD 工具选择
- Docker 配置
- Kubernetes 部署
- 自动化流水线实现

---

# 十二、Dependencies（依赖关系）

Depends On：

- 404 Git Convention
- 405 Branch Convention
- 406 Commit Convention
- 411 Development Workflow
- 412 Review Workflow

Affects：

- 全部版本发布
- 全部部署流程
- 全部项目生命周期

---

# 十三、本章总结

Release Workflow 定义了 AI Drama Factory 的标准发布流程。

Factory 不追求：

快速上线。

而追求：

稳定。

一致。

可恢复。

可追溯。

未来。

任何正式版本。

都应经过统一发布流程。

确保整个 Factory 长期稳定演进。

---

**End**