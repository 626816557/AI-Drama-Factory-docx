

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

> **AI Drama Factory 应采用什么样的统一命名规范？**

Naming Convention 定义整个项目的命名规则。

包括：

- 目录
- 文件
- 类
- 方法
- 数据库
- API
- 配置
- Workshop
- AI 模块

统一命名。

是整个 Factory 可维护性的基础。

---

# 二、设计目标（Purpose）

统一命名的目标不是形式统一。

而是：

- 易读
- 易理解
- 易搜索
- 易维护
- 易协作

任何名称。

都应能够准确表达自身职责。

---

# 三、核心原则（Core Principles）

Factory 遵循以下命名原则。

## Meaningful（语义明确）

名称应准确表达职责。

例如：

```
DirectorWorkshop
```

优于：

```
Director
```

因为它明确表达：

这是一个 Workshop。

---

## Consistent（一致性）

同一种对象。

必须采用统一命名方式。

例如：

全部使用：

```
Project

Workshop

Adapter

Repository
```

不要混用：

```
Service

Manager

Handler

Processor
```

表达同一种职责。

---

## Predictable（可预测）

开发人员无需搜索。

即可预测：

文件名称。

类名称。

目录名称。

---

## Simple（保持简单）

优先使用行业通用命名。

避免创造新的缩写。

例如：

使用：

```
Configuration
```

而不是：

```
Cfg
```

---

# 四、目录命名（Directory Naming）

目录统一使用：

```
kebab-case
```

例如：

```
frontend/

backend/

workshops/

asset-generation/

video-generation/

knowledge-base/
```

禁止：

```
VideoGeneration/

videoGeneration/

video_generation/
```

---

# 五、文件命名（File Naming）

普通文件统一使用：

```
kebab-case
```

例如：

```
project-service.ts

director-workshop.ts

video-renderer.ts
```

Markdown 文档：

保持：

```
300-overall-architecture.md

401-directory-convention.md
```

编号始终保留。

方便长期维护。

---

# 六、类命名（Class Naming）

类统一使用：

```
PascalCase
```

例如：

```
ProjectService

DirectorWorkshop

AssetGenerator

CharacterRepository
```

类名称必须使用名词。

避免动词。

---

# 七、接口命名（Interface Naming）

接口统一使用：

```
PascalCase
```

例如：

```
Project

Workshop

StorageProvider

ImageGenerator
```

不建议增加：

```
IProject
```

前缀。

保持现代 TypeScript 风格。

---

# 八、函数命名（Function Naming）

函数统一使用：

```
camelCase
```

例如：

```
createProject()

generateStory()

publishVideo()

calculateScore()
```

函数必须使用动词开头。

表达动作。

---

# 九、变量命名（Variable Naming）

变量统一使用：

```
camelCase
```

例如：

```
projectId

currentWorkshop

generatedAssets
```

变量名称应完整表达含义。

避免：

```
data

obj

tmp

value
```

---

# 十、常量命名（Constant Naming）

常量统一使用：

```
UPPER_SNAKE_CASE
```

例如：

```
MAX_WORKSHOP_COUNT

DEFAULT_LANGUAGE

AI_PROVIDER_TIMEOUT
```

所有常量保持统一风格。

---

# 十一、数据库命名（Database Naming）

表名：

统一使用：

```
snake_case
```

例如：

```
projects

story_scripts

character_profiles

video_assets
```

字段：

统一使用：

```
snake_case
```

例如：

```
created_at

updated_at

project_id
```

---

# 十二、API 命名（API Naming）

REST API：

统一使用：

```
/projects

/projects/:id

/workshops

/assets

/videos
```

使用资源名称。

避免：

```
/getProjects

/createProject
```

REST 风格由 HTTP Method 表达动作。

---

# 十三、Workshop 命名（Workshop Naming）

所有 Workshop：

统一使用：

```
XXXWorkshop
```

例如：

```
MarketWorkshop

StoryWorkshop

DirectorWorkshop

PublishingWorkshop
```

避免：

```
MarketService

MarketManager
```

统一职责表达。

---

# 十四、Adapter 命名（Adapter Naming）

所有 Adapter：

统一使用：

```
XXXAdapter
```

例如：

```
OpenAIAdapter

SeedanceAdapter

StorageAdapter

TranslationAdapter
```

保持统一。

---

# 十五、AI Provider 命名

AI Provider 保持官方名称。

例如：

```
OpenAI

Claude

Gemini

DeepSeek

Seedance
```

不要自行缩写。

---

# 十六、禁止命名（Forbidden Naming）

禁止使用：

```
temp

temp2

test-final

new

new2

backup-final

old

misc

other
```

任何名称。

都必须表达真实职责。

---

# 十七、命名设计原则（Design Principles）

Factory 坚持：

## Readability First

优先可读性。

---

## Consistency First

优先统一。

---

## Explicit Better Than Implicit

名称明确。

优于隐含。

---

## Long-term Maintainability

命名应支持长期维护。

而不是只方便当前开发。

---

# 十八、Non-Goals（非目标）

本章不负责：

- Git 规范（404）
- Commit Message（406）
- Prompt 命名（407）
- 数据库结构（409）

---

# 十九、Dependencies（依赖关系）

Depends On：

- 401 Directory Convention

Affects：

- 全部源码
- 全部数据库
- 全部 API
- 全部 Workshop
- 全部文档

---

# 二十、本章总结

Naming Convention 是 AI Drama Factory 的统一语言。

统一命名。

不仅提高代码质量。

更降低沟通成本。

未来。

任何开发人员。

任何 AI。

任何自动生成代码。

都应遵循统一命名规范。

---

**End**