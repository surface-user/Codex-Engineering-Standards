# Codex Engineering Standards

A reusable AI-assisted software engineering standard for Codex and other coding agents.

## 1. Introduction

Codex Engineering Standards is a reusable engineering workflow designed to improve the consistency, maintainability, and reliability of AI-assisted software development.

It establishes common engineering principles and development workflows across different software projects and technology stacks.

The standards are designed for individual developers who use AI coding agents to develop, maintain, test, and deliver software projects.

The goal is not to enforce unnecessary procedures, but to help AI agents work with clear requirements, structured task management, effective collaboration, and verifiable engineering results.

## 2. Core Objectives

- Establish consistent engineering practices across projects.
- Improve requirement analysis and project understanding.
- Standardize project documentation and task management.
- Enable effective multi-agent collaboration.
- Integrate Git, Pull Requests, and Continuous Integration into development workflows.
- Improve implementation verification and delivery reliability.
- Reduce repetitive instructions and manual coordination.

## 3. Supported Technology Stacks

The standards are technology-independent and can be adapted to different development environments, including:

- Python
- C++
- C#
- Flutter / Dart
- Unity
- Other software development technologies

Projects should follow the official or established directory conventions of their respective ecosystems.

The standards do not enforce a universal source-code directory structure.

Monorepo is preferred when multiple technology stacks or closely related components benefit from unified repository management.

## 4. Repository Structure

```text
Codex-Engineering-Standards/
│
├── README.md
├── AGENTS.md
│
├── global/
│   ├── AGENTS.md
│   └── settings-entry.md
│
├── guides/
│   ├── project-initialization.md
│   └── engineering-workflow.md
│
└── templates/
    ├── project-AGENTS.md
    └── docs/
        ├── requirements.md
        ├── architecture.md
        ├── task.md
        └── ADR.md
```

Each directory has a distinct responsibility:

| Directory | Responsibility |
|---|---|
| `global/` | Global engineering instructions |
| `guides/` | Detailed engineering procedures |
| `templates/` | Reusable project documentation formats |

The repository structure may evolve as the standards develop.

Not every project needs to adopt every document or directory.

## 5. Documentation Hierarchy

The engineering standards use three levels:

### Global Instructions

Define engineering behavior and constraints that apply across projects.

Location: `global/AGENTS.md`

### Project Instructions

Define project-specific goals, technology stacks, directory structures, and development constraints.

Location: Project root `AGENTS.md`

### Project Development Documentation

Describe the actual project requirements, architecture, current tasks, and important architecture decisions.

Location: Project `docs/`

Detailed procedures and reusable document formats are maintained separately under `guides/` and `templates/`.

## 6. Getting Started

To use these standards:

1. Clone this repository to your local development environment.
2. Configure the global AGENTS.md entry in your Codex environment.
3. Point the global entry to the complete instructions under `global/AGENTS.md`.
4. When entering a software project, let Codex inspect its project-level AGENTS.md and relevant development documentation.
5. Use the appropriate guides and templates when necessary.

Local reference path:

```text
D:\computer_work\Codex-Engineering-Standards
```

The actual path may differ between development environments.

## 7. Design Principles

This project follows several fundamental principles:

- **Practicality:** Every rule and document must provide clear engineering value.
- **Progressive Evolution:** Engineering standards should evolve with project complexity.
- **Technology Adaptability:** Follow established technology-specific conventions.
- **Clear Responsibilities:** Every document and module must have a defined purpose.
- **Controlled Autonomy:** Agents can make engineering decisions within authorized boundaries.
- **Human Oversight:** Important requirements, architecture decisions, and high-risk operations remain subject to user authorization.
- **Verifiability:** Development results must be supported by actual verification evidence.

## 8. Project Status

This repository is being established progressively.

Its initial development focuses on:

1. Global engineering instructions.
2. Project initialization procedures.
3. Multi-agent development workflows.
4. Git, PR, and CI integration.
5. Reusable project documentation templates.

The standards will be refined through practical use and feedback from real software projects.

## 9. License

To be determined.