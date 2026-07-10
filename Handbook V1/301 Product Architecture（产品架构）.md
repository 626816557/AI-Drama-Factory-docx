

> Version：V1.0  
> Status：Draft  
> Last Update：2026-07-01  
> Owner：AI Drama Factory

---

# 一、本文档回答什么问题？

本文档回答：

> **AI Drama Factory 作为一个软件产品，由哪些产品模块组成？**

Product Architecture 关注的是产品形态。

它不讨论代码如何实现。

也不讨论数据库如何设计。

这些将在后续章节说明。

---

# 二、产品定位

AI Drama Factory 是一套：

> **AI 内容生产操作系统（AI Content Operating System）**

它不是单个工具。

不是单个脚本。

不是单个 AI 工作流。

而是一套完整产品。

用于管理：

- 内容发现
- 内容策划
- AI 生产
- 素材管理
- 视频生成
- 发布运营
- 数据分析
- 持续学习

---

# 三、产品核心对象

AI Drama Factory 的核心产品对象是：

> **Project（项目）**

一个 Project 代表一个完整内容生产生命周期。

例如：

一部短剧。

一个系列。

一个 IP。

未来所有功能都围绕 Project 运转。

---

# 四、产品模块

AI Drama Factory 产品层由八个核心模块组成。

```
Dashboard

↓

Project Center

↓

Workshop Center

↓

Asset Center

↓

Video Center

↓

Publishing Center

↓

Analytics Center

↓

Learning Center
```

---

# 五、Dashboard（总控台）

Dashboard 是整个 Factory 的首页。

负责展示：

- 今日生产状态
- 项目数量
- 任务进度
- 成本
- 收益
- GPU 状态
- 爆款预测
- 风险提醒

Dashboard 的目标是：

让用户一眼看懂整个工厂当前状态。

---

# 六、Project Center（项目中心）

Project Center 管理所有 Project。

包括：

- 创建 Project
- 查看 Project 状态
- 查看 Project 生命周期
- 查看剧本
- 查看图片
- 查看视频
- 查看发布数据

Project Center 是整个产品的核心页面。

---

# 七、Workshop Center（车间中心）

Workshop Center 管理所有生产车间。

包括：

- Market Intelligence
- Story Intelligence
- Validation
- Director
- Asset Generation
- Video Generation
- Audio
- Subtitle
- Publishing
- Analytics
- Learning

每个 Workshop 都应具备：

- 运行状态
- 输入
- 输出
- 日志
- 成功率
- 失败原因
- 重新执行能力

---

# 八、Asset Center（素材中心）

Asset Center 管理所有生产素材。

包括：

- 图片
- 视频片段
- 音频
- 字幕
- 角色参考
- 场景参考
- Prompt
- 模板

Asset Center 不是文件夹。

而是素材资产管理系统。

---

# 九、Video Center（视频中心）

Video Center 管理最终视频生产。

包括：

- 镜头组合
- 配音
- 字幕
- BGM
- 音效
- 转场
- 成片
- 版本管理

Video Center 的目标是：

将分散素材组织成可发布内容。

---

# 十、Publishing Center（发布中心）

Publishing Center 管理内容发布。

包括：

- 平台选择
- 标题
- 封面
- 标签
- 发布时间
- 发布状态
- 发布失败处理

未来支持多平台发布。

例如：

- TikTok
- YouTube Shorts
- Instagram Reels
- Facebook

---

# 十一、Analytics Center（数据中心）

Analytics Center 负责分析内容表现。

包括：

- 播放量
- 完播率
- 点赞率
- 评论率
- 分享率
- 追更率
- ROI
- 爆款评分

数据结果将反馈给 Learning Center。

---

# 十二、Learning Center（学习中心）

Learning Center 负责把数据转化为经验。

包括：

- 爆款规律
- Hook 规律
- 题材表现
- 角色偏好
- 平台差异
- 地区差异
- Prompt 优化
- 内容规则更新

Learning Center 是 Factory 越来越聪明的关键。

---

# 十三、产品关系

AI Drama Factory 产品模块关系如下：

```
Dashboard
    │
    ▼
Project Center
    │
    ▼
Workshop Center
    │
    ▼
Asset / Video / Publishing
    │
    ▼
Analytics
    │
    ▼
Learning
    │
    ▼
Next Project
```

整个产品围绕 Project 形成闭环。

---

# 十四、产品设计原则

AI Drama Factory 产品层遵循以下原则：

## 1、Project First

所有功能围绕 Project 组织。

---

## 2、Visual First

所有核心能力最终必须可视化。

不能长期依赖命令行。

---

## 3、Status First

每个 Project、Workshop、Task 都必须有明确状态。

---

## 4、Data First

任何生产结果都必须沉淀数据。

---

## 5、Feedback First

任何发布结果都必须反馈到下一轮生产。

---

# 十五、未来演进

未来 Product Architecture 将支持：

- 多用户
- 多团队
- 权限系统
- SaaS 化
- 插件市场
- 多语言界面
- 企业版
- 移动端控制台

但当前阶段优先完成：

> 单人可用、流程清晰、状态可视化的本地版本。

---

# 十六、本章总结

Product Architecture 定义 AI Drama Factory 作为产品的基本形态。

整个产品不围绕脚本。

不围绕文件。

不围绕单个 AI 模型。

而围绕：

> **Project 生命周期**

展开。

未来所有功能，都应服务于 Project 的创建、生产、发布、分析和持续优化。

---

**End**