# ADR - Architecture Decision Record

本文档用于记录项目中的重要架构决策及其变更历史。

只有经过用户确认的重要架构决策才创建 ADR。

普通实现细节、函数重构和常规代码优化不需要创建 ADR。

---

# ADR-0001: [Decision Title]

- **Status:** Proposed
- **Date:** YYYY-MM-DD
- **Related Requirements:** [FR-001, if applicable]
- **Related Tasks:** [Task ID, if applicable]
- **Supersedes:** None
- **Superseded By:** None

## 1. Context

描述当前遇到的问题、技术背景和需要作出决策的原因。

## 2. Decision Drivers

列出影响决策的重要因素。

例如：

- 技术可行性。
- 性能要求。
- 系统兼容性。
- 开发和维护成本。
- 安全性。
- 可扩展性。

## 3. Considered Options

### Option A: [Option Name]

简要说明方案及其优缺点。

### Option B: [Option Name]

简要说明方案及其优缺点。

## 4. Decision

明确记录最终采用的方案。

说明该决策具体改变了什么，以及适用范围。

## 5. Rationale

解释为什么选择该方案，以及为什么没有选择其他方案。

## 6. Consequences

记录该决策带来的重要影响。

**Positive:**
- [Positive consequence]

**Negative:**
- [Negative consequence]

**Risks:**
- [Potential risks]

## 7. Follow-up Actions

记录实施该决策所需要完成的重要后续工作。

- [ ] [Action 1]
- [ ] [Action 2]

---

# ADR Status

使用以下状态：

- Proposed: 已提出，尚未获得用户确认。
- Accepted: 已经用户确认并决定采用。
- Rejected: 已评估，但决定不采用。
- Superseded: 已被后续架构决策替代。

## ADR Management Rules

1. ADR 使用永久递增编号，例如 ADR-0001、ADR-0002。
2. 已有 ADR 不得随意删除。
3. 重要架构决策必须先向用户说明并获得确认。
4. 用户确认后，主 Agent 创建对应 ADR。
5. 原有决策被替代时，创建新的 ADR。
6. 被替代的 ADR 标记为 Superseded，并关联新 ADR。
7. ADR 记录决策及其理由，不代替 architecture.md 描述实际架构。
8. 普通实现调整不需要创建 ADR。