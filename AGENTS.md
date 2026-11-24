# AGENTS.md

## 1. Project Overview

Codex-Engineering-Standards is a repository for maintaining reusable AI-assisted software engineering standards.

It provides global instructions, engineering workflow guides, and project documentation templates for Codex and other coding agents.

The repository itself is maintained as a long-term engineering standards project.

## 2. Project Objectives

- Maintain consistent and practical global engineering instructions.
- Provide reusable project initialization and development workflows.
- Maintain concise and useful documentation templates.
- Avoid duplicated, contradictory, or unnecessary rules.
- Improve the standards through practical validation and feedback.

## 3. Repository Structure

```text
Codex-Engineering-Standards/
├── README.md
├── AGENTS.md
├── global/
│   ├── AGENTS.md
│   ├── chapters/  (eight standards chapters)
│   └── settings-entry.md
├── guides/
│   ├── project-initialization.md
│   └── engineering-workflow.md
└── templates/
    ├── project-AGENTS.md
    └── docs/
        ├── requirements.md
        ├── architecture.md
        ├── task.md
        └── ADR.md
```

This structure represents the intended organization. Update this document when the actual repository structure changes.

## 4. Documentation Responsibilities

Each document must have a clear and independent responsibility.

- `README.md`: Introduces the repository and explains how to use it.
- [`global/AGENTS.md`](global/AGENTS.md): Defines the baseline and when to read each global standards chapter.
- `global/chapters/`: Contains the eight global standards chapters. The index links to each chapter and defines its reading trigger.
- `global/settings-entry.md`: Contains the concise global entry configured in the Codex environment.
- `guides/`: Explains detailed engineering procedures.
- `templates/`: Provides reusable project documentation formats.

Avoid duplicating rules across documents.

When modifying a rule, inspect its related references and update affected documents consistently.

## 5. Development Constraints

- MUST preserve the engineering decisions explicitly confirmed by the repository owner.
- MUST NOT change confirmed global engineering rules without user authorization.
- MUST maintain consistency between global instructions, guides, and templates.
- MUST prioritize practical usability over documentation completeness.
- MUST avoid unnecessary files, directories, abstractions, and procedures.
- MUST NOT create templates merely to fill the repository structure.
- SHOULD reuse existing documents rather than create duplicates.
- SHOULD keep documentation concise and actionable.

## 6. Change Management

When modifying engineering standards:

1. Identify the purpose and scope of the change.
2. Inspect related instructions and documentation.
3. Check for duplicated or conflicting rules.
4. Preserve existing confirmed decisions unless explicitly authorized to change them.
5. Update affected documents.
6. Review consistency across the repository.
7. Summarize changes and unresolved issues.

Significant changes to global engineering rules require explicit confirmation from the repository owner before implementation.

## 7. Verification

After modifying repository documentation:

- Check Markdown formatting and structure.
- Verify internal file references and paths.
- Check consistency between related documents.
- Identify outdated examples and directory references.
- Report missing or incomplete documents honestly.

Do not claim that a document or workflow has been validated unless the relevant checks have actually been performed.

## 8. Git Conventions

Use Conventional Commits for repository changes.

Examples:

- `feat(guides): add multi-agent workflow guide`
- `docs(global): refine authorization rules`
- `fix(templates): correct task identifier format`
- `refactor(structure): simplify documentation layout`

Preserve the existing Git history and avoid unrelated modifications.
