# Project Initialization Guide

本指南规定 Codex 如何初始化新软件项目，以及如何为已有项目补充工程规范。

核心目标是：通过逐步需求分析、技术调研和架构设计，建立与实际项目相匹配的工程结构和开发文档。

不要求所有项目采用相同的技术栈、目录结构或架构模式。

---

# 1. Initialization Principles

## 1.1 Progressive Initialization

项目初始化应根据实际需求逐步推进。

不要在用户只提供一句项目描述时，就直接生成完整架构、目录结构和开发任务。

应先理解用户意图，再逐步完成需求、技术选型、架构设计和工程初始化。

## 1.2 Practical Documentation

每份开发文档必须具有明确的工程价值。

- 不创建没有实际用途的文档。
- 不为了满足目录模板而创建空文件。
- 优先遵循成熟技术栈的官方目录惯例。
- 项目复杂度决定工程规范的完整程度。
- 简单项目不强制建立完整文档体系。

## 1.3 Confirmed Information

需求分析过程中，必须区分：

- CONFIRMED：用户已经明确确认的信息。
- PENDING：仍然需要确认的信息。
- ASSUMPTION：Agent 为推进分析暂时采用的假设。

未经用户确认的假设不得写成正式需求或已实施的架构事实。

## 1.4 New and Existing Projects

区分两种初始化场景：

**New Project**

从项目目标和需求开始，逐步建立工程结构。

**Existing Project**

先检查现有代码、配置和文档，再决定如何补充工程规范。

不得为了套用初始化模板而破坏已有项目结构或删除历史资料。

---

# 2. Phase 1 — Project Understanding

## 2.1 Collect Initial Information

接收用户的初始项目描述。

优先理解：

- 项目要解决什么问题？
- 主要面向什么用户？
- 用户希望实现什么结果？
- 项目的主要使用场景是什么？
- 是否存在明确的技术或平台限制？

不要求用户一次性提供完整信息。

## 2.2 Structured Requirement Analysis

根据用户描述生成需求理解摘要。

建议使用：

### Confirmed

记录用户已经明确确认的项目事实。

### Pending

记录影响技术选型、架构或功能设计的待确认问题。

### Assumptions

记录 Agent 暂时采用的分析假设。

## 2.3 Clarification

Agent 应优先识别会影响整体设计的问题。

例如：

- 是否需要本地或云端数据存储？
- 是否需要账号系统？
- 是否支持多设备同步？
- 是否需要离线使用？
- 是否需要第三方服务？
- 是否存在性能或安全要求？

每次优先询问一个关键问题，并根据用户回答继续完善需求理解。

必要时向用户解释相关技术概念和不同方案的优缺点。

## 2.4 Phase Output

本阶段形成项目需求理解摘要。

不要求立即创建正式 requirements.md。

进入下一阶段的条件：

- 项目主要目标已经明确。
- 核心使用场景已经理解。
- 关键歧义已经得到处理，或被明确标记为待确认。

---

# 3. Phase 2 — Technical Investigation

## 3.1 Technology Selection

根据项目需求分析技术选型。

考虑：

- 编程语言。
- 开发框架。
- 目标平台。
- 数据存储方案。
- 第三方依赖。
- 构建和部署环境。
- 开源项目和成熟解决方案。

不要为了使用新技术而引入不必要的依赖。

## 3.2 Open-source Research

当项目涉及复杂技术或已有成熟开源方案时，应进行适当调研。

重点关注：

- 项目是否仍在维护。
- 是否满足实际功能需求。
- 是否存在兼容性问题。
- 许可证是否允许当前用途。
- 是否存在已知安全风险。
- 是否能够合理集成到现有架构。

优先复用成熟解决方案，不要重复开发已有的基础能力。

## 3.3 Feasibility Analysis

分析技术方案是否可行。

至少考虑：

- 技术限制。
- 平台兼容性。
- 依赖关系。
- 开发成本。
- 长期维护成本。
- 主要风险。

对于存在明显争议的技术选型，应向用户解释不同方案。

## 3.4 Phase Output

形成技术选型和可行性分析结果。

此阶段不要求生成独立的技术调研报告 Markdown。

---

# 4. Phase 3 — Requirements Specification

## 4.1 Requirement Organization

将已确认的项目需求整理成正式功能需求。

以用户可观察的功能和业务行为为中心，而不是按照源代码模块划分需求。

功能需求使用永久编号：

- FR-001
- FR-002
- FR-003

必要时使用：

- BR：Business Rules
- NFR：Non-functional Requirements

## 4.2 Gherkin Scenarios

对于具有明确业务行为的功能，可以使用 Given-When-Then 描述验收场景。

Example:

Feature: Import Learning Material

Scenario: Successfully import a PDF file

Given the user selects a valid PDF file
When the user confirms the import
Then the system stores the file
And displays the imported material

Gherkin 描述的是功能行为和预期结果。

不要将具体代码实现方式写成用户功能需求。

## 4.3 Requirement Validation

检查：

- 是否存在重复需求。
- 是否存在相互矛盾的需求。
- 是否缺少关键业务场景。
- 是否存在无法验证的描述。
- 是否存在未经用户确认的假设。

重大需求歧义必须向用户询问。

## 4.4 Create requirements.md

用户确认需求后，创建：

`docs/requirements.md`

后续需求变更必须遵循全局 AGENTS.md 中的需求管理规则。

---

# 5. Phase 4 — Architecture Design

## 5.1 Module Identification

根据业务职责识别系统模块。

考虑：

- 每个模块负责什么？
- 模块之间如何协作？
- 哪些能力需要跨模块共享？
- 哪些模块具有独立的数据管理职责？
- 是否存在不必要的依赖关系？

不要为了追求模块数量而过度拆分。

## 5.2 Architecture Analysis

根据项目复杂度分析：

- 模块职责。
- 模块依赖关系。
- 公共接口。
- 数据流。
- 关键业务流程。
- 必要的内部架构分层。

优先采用低耦合设计，并根据实际需要决定是否引入分层架构、Repository、依赖注入或事件机制。

不强制使用某一种架构模式。

## 5.3 Architecture Diagrams

当系统存在多个业务模块或复杂依赖关系时，可以使用 UML、Mermaid 等工具辅助表达。

根据需要绘制：

- 模块关系图。
- 依赖关系图。
- 数据流图。
- 关键业务流程图。

图表应帮助理解架构，而不是为了形式而生成。

## 5.4 Architecture Validation

检查：

- 是否存在循环依赖。
- 是否存在职责重叠。
- 公共模块是否具有明确边界。
- 模块接口是否足够清晰。
- 架构是否满足已经确认的需求。
- 是否存在不必要的复杂度。

## 5.5 Create architecture.md

架构方案确认后，创建：

`docs/architecture.md`

该文件记录当前已经确认并实际实施的架构。

尚未实施的架构决策应通过 ADR 和开发任务管理，不得提前描述为当前实际架构。

---

# 6. Phase 5 — Project Engineering Setup

## 6.1 Technology-specific Structure

根据实际技术栈建立项目目录。

遵循官方或成熟生态惯例。

Examples:

Python:
- src/
- tests/
- pyproject.toml

Flutter:
- lib/
- test/
- pubspec.yaml

C++:
- src/
- include/
- tests/
- CMakeLists.txt

C#:
- src/
- tests/
- .sln / .csproj

Unity:
- Assets/
- Packages/
- ProjectSettings/

这些只是参考，不是强制目录模板。

## 6.2 Monorepo Consideration

当项目包含多种技术栈或多个紧密关联的应用和服务时，优先评估 Monorepo。

例如：

- Flutter 桌面应用。
- Python Agent 服务。
- C++ 底层引擎。

根据模块耦合、部署方式、权限和版本管理需求决定是否使用单仓库。

如果建议拆分为多个仓库，必须向用户解释原因和影响。

## 6.3 Project AGENTS.md

创建项目根目录：

`AGENTS.md`

至少说明：

- Project Overview
- Project Goals
- Technology Stack
- Project Structure
- Development Constraints
- Quality Assurance
- Git Workflow
- Documentation

子目录 AGENTS.md 仅在存在特殊局部开发约束时建立。

## 6.4 README.md

创建根目录 README.md。

介绍：

- 项目用途。
- 主要功能。
- 技术栈。
- 安装方式。
- 运行方式。
- 开发文档入口。

README 必须根据实际项目状态维护。

## 6.5 Testing Setup

中大型项目必须规划自动化测试入口。

根据技术栈配置适当的测试工具。

不要要求项目初期就拥有大量测试代码。

## 6.6 Optional Directories

根据实际需要建立：

- scripts/
- artifacts/
- .local/

不要创建没有实际用途的空目录。

---

# 7. Phase 6 — Task Planning

## 7.1 Task Breakdown

根据 requirements.md 和 architecture.md 制定初始开发计划。

主 Agent 负责：

- 识别独立开发目标。
- 判断任务粒度。
- 分析任务依赖。
- 判断并行可行性。
- 安排开发顺序。

不要求将每个功能拆分成大量小任务。

## 7.2 Task Identifiers

使用统一任务编号：

`YYYYMMDD-HHmm-NNN`

其中 NNN 表示同一创建批次中的任务序号。

同一项目由主 Agent 统一分配正式任务编号。

## 7.3 Create task.md

创建：

`docs/task.md`

记录：

- Task ID
- Task Description
- Status
- Priority
- Related Requirements
- Dependencies

正式任务状态：

- READY
- WORKING
- WAITING
- FINISH

正式任务只由主 Agent 管理。

Worker 内部子任务不进入 task.md。

## 7.4 Initial Development Plan

向用户展示：

- 初始开发任务。
- 任务依赖关系。
- 建议的开发顺序。
- 可以并行的工作。
- 主要技术风险。

---

# 8. Phase 7 — Initialization Review

项目初始化完成后，主 Agent 必须进行一次整体检查。

## 8.1 Documentation Review

检查：

- README.md 是否准确。
- AGENTS.md 是否描述实际技术栈和目录结构。
- requirements.md 是否符合用户确认的需求。
- architecture.md 是否反映实际架构。
- task.md 是否包含合理的初始开发任务。
- ADR 是否只记录已经确认的重要架构决策。

## 8.2 Engineering Structure Review

检查：

- 技术栈配置是否正确。
- 依赖是否能够正常恢复。
- 基本构建是否可行。
- 测试入口是否可用。
- 目录结构是否符合技术栈惯例。
- 是否存在不必要的文件和目录。

## 8.3 Initialization Report

向用户提供简洁的初始化总结：

1. Project Overview
2. Confirmed Technology Stack
3. Directory Structure
4. Created Documentation
5. Architecture Summary
6. Initial Development Tasks
7. Known Risks
8. Pending Decisions

## 8.4 Completion

项目初始化不以生成多少份 Markdown 为完成标准。

当项目目标、核心需求、技术选型、架构和初始开发任务已经得到合理确认，必要工程配置已经建立，并且初始化结果经过检查后，可以结束初始化阶段。

非关键问题可以保留为 PENDING，不必阻塞所有后续开发。

最终由用户 Review 初始化结果。

---

# 9. Existing Project Initialization

当用户要求为已有项目补充工程规范时，不得直接套用新项目初始化流程。

应先：

1. 检查现有 AGENTS.md 和开发文档。
2. 分析实际技术栈和目录结构。
3. 检查当前代码与配置。
4. 识别现有架构和模块关系。
5. 对照现有文档检查不一致。
6. 识别缺失但具有实际价值的工程文档。
7. 向用户说明现状和建议的规范补充方案。

遵循渐进式演进原则：

- 保留有价值的现有结构。
- 不随意重命名或移动已有文件。
- 不删除历史文档和测试证据。
- 不强制引入完整工程文档体系。
- 优先补齐真正缺失的工程管理能力。

涉及重大结构调整时，先向用户解释并取得确认。

---

# 10. Final Principles

Project initialization should produce a usable engineering foundation, not a collection of documents.

Every document, directory, tool, and workflow must have a clear purpose.

The final structure must reflect the actual project, support future development, and remain understandable to both developers and coding agents.