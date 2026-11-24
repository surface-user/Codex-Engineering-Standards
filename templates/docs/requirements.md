# Requirements

本文档记录项目当前有效的功能需求、业务规则和必要的非功能需求。

需求描述以用户可观察的功能和业务行为为中心，不规定具体代码实现方式。

---

# 1. Functional Requirements

本章节记录项目需要实现的功能。

每项独立功能使用唯一编号 `FR-001`、`FR-002`、`FR-003`，按照需求首次创建的顺序分配。

一个功能可以包含多个相关场景，不要求每个场景都单独创建需求编号。

## FR-001 - [功能名称]

**Description:**

简要说明该功能需要实现什么，以及用户能够获得什么结果。

**Scenarios:**

### Scenario 1: [正常业务场景]

**Given** [场景成立的前置条件]

**When** [用户执行的操作或触发的事件]

**Then** [系统应该产生的结果]

### Scenario 2: [异常或边界场景]

**Given** [场景成立的前置条件]

**When** [用户执行的操作或触发的事件]

**Then** [系统应该产生的结果]

---

## FR-002 - [功能名称]

**Description:**

[功能描述]

**Scenarios:**

### Scenario 1: [场景名称]

**Given** [前置条件]

**When** [操作或事件]

**Then** [预期结果]

---

# 2. Business Rules

本章节记录对多个功能具有约束作用的业务规则。

只有存在独立业务规则时才需要填写。

使用永久编号：

- BR-001
- BR-002
- BR-003

## BR-001 - [业务规则名称]

**Description:**

说明规则内容、适用范围和限制条件。

**Related Requirements:**

- FR-001
- FR-002

---

# 3. Non-functional Requirements

本章节记录功能之外的质量要求和系统约束。

根据项目实际需要选择性填写，不要求每个项目都包含全部类型。

可涉及：

- Performance：性能要求。
- Security：安全要求。
- Reliability：可靠性要求。
- Compatibility：兼容性要求.
- Availability：可用性要求。
- Scalability：可扩展性要求.
- Accessibility：可访问性要求。

使用永久编号：

- NFR-001
- NFR-002
- NFR-003

## NFR-001 - [非功能需求名称]

**Description:**

说明具体的质量要求或系统约束。

**Acceptance Criteria:**

说明如何判断该要求是否满足。

**Related Requirements:**

- FR-001

---

# 4. Requirement Change Rules

本章节规定需求的生命周期管理。

## 4.1 Requirement Modification

修改已有需求时：

- 保留原有需求编号。
- 更新对应功能描述和验收场景。
- 检查关联功能和业务规则是否受到影响。
- 重大需求变化必须经过用户确认。

## 4.2 Requirement Addition

新增功能时：

- 分配新的需求编号。
- 检查是否存在重复或相似需求。
- 明确功能描述和必要的验收场景。
- 经过用户确认后纳入正式需求文档。

## 4.3 Requirement Deletion

删除需求时：

- 必须经过用户确认。
- 删除后永久保留该编号的作废记录。
- 已作废的需求编号不得重新使用。
- 检查关联任务、功能和接口是否需要调整。

## 4.4 Requirement Traceability

需求编号用于关联正式开发任务和相关 PR。

- requirements.md 只记录当前有效需求及必要的编号作废信息。
- docs/task.md 记录当前开发任务及其关联需求。
- PR 通过任务编号和需求编号关联具体修改。
- 不在 requirements.md 中记录开发进度或完成状态。

---

# 5. Documentation Constraints

- 本文档只描述项目需要实现什么。
- 不记录具体源代码目录和文件职责。
- 不规定具体技术栈和依赖版本。
- 不记录模块之间的详细接口定义。
- 不记录开发任务和任务完成状态。
- 不记录架构决策及其演进过程。
- 不将未经确认的假设写成正式需求。

技术栈和项目开发约束由项目根目录 AGENTS.md 记录。

系统架构和模块关系由 architecture.md 记录。

开发任务和进度由 task.md 管理。

重要架构决策由 ADR 记录。