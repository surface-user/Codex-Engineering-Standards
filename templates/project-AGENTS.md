# Project AGENTS.md

## 1. Project Overview

**Project Name:** [Project Name]

**Description:** [Brief description of the project]

**Primary Goals:**
- [Goal 1]
- [Goal 2]

**Target Users:** [Intended users]

**Target Platforms:** [Supported platforms]

## 2. Technology Stack

| Category | Technology | Version |
|---|---|---|
| Language | [Language] | [Version] |
| Framework | [Framework] | [Version] |
| Database | [Database] | [Version] |
| Build System | [Build Tool] | [Version] |
| Other Dependencies | [Dependencies] | [Versions] |

Only include technologies actually used by the project.

## 3. Project Structure

```text
[Project Root]/
├── README.md
├── AGENTS.md
├── docs/
│   ├── requirements.md
│   ├── architecture.md
│   ├── task.md
│   ├── adr/
│   └── guides/
├── [Source Directory]/
├── [Test Directory]/
└── dev/
    ├── README.md
    ├── records/
    └── archive/
```

Replace this example with the actual project directory structure.

Describe the responsibilities of important directories and modules.

Follow the established conventions of the project's technology stack. Do not create directories solely to match this example.

## 4. Module Responsibilities

| Module | Responsibility | Important Dependencies |
|---|---|---|
| [Module A] | [Description] | [Dependencies] |
| [Module B] | [Description] | [Dependencies] |
| [Shared Module] | [Description] | [Dependencies] |

Keep this section focused on major business modules and important shared capabilities.

Detailed architecture and interface relationships belong in `docs/architecture.md`.

## 5. Development Environment

**Required Environment:**
- Operating System: [Supported OS]
- Runtime / SDK: [Required versions]
- Required Tools: [Development tools]

**Dependency Installation:**

```bash
[Dependency installation command]
```

**Development Startup:**

```bash
[Development startup command]
```

**Build:**

```bash
[Build command]
```

## 6. Quality Assurance

Document the actual verification commands supported by this project.

| Check | Command | Purpose |
|---|---|---|
| Format | [Command] | Code formatting |
| Lint / Static Analysis | [Command] | Static checks |
| Type Check | [Command or N/A] | Type verification |
| Unit Tests | [Command] | Unit testing |
| Integration Tests | [Command or N/A] | Integration testing |
| Build | [Command] | Build verification |

Only include applicable checks.

Do not invent commands or claim that a verification tool is configured when it is not.

## 7. Project-specific Development Constraints

Record constraints that are specific to this project.

Examples:

- Required runtime or SDK versions.
- Database access restrictions.
- Public API compatibility requirements.
- Platform-specific limitations.
- Resource management requirements.
- Important module interaction constraints.
- Special testing or build requirements.

Do not duplicate rules already defined in the global engineering standards.

## 8. Git Workflow

**Main Branch:** [Branch Name]

**Development Branch Convention:** [Branch naming rules]

**Commit Convention:** Conventional Commits

**PR Requirements:** [Project-specific review and CI requirements]

Document only project-specific Git settings. Follow the global engineering standards for general Git, Worktree, PR, and authorization rules.

## 9. Documentation

The project's formal development documentation is maintained under `docs/`.

| Document | Responsibility |
|---|---|
| `docs/requirements.md` | Confirmed functional and non-functional requirements |
| `docs/architecture.md` | Actual implemented system architecture |
| `docs/task.md` | Current formal development tasks |
| `docs/adr/` | Important confirmed architecture decisions |
| `docs/guides/` | Long-term project-specific development guides |

Development history and valuable evidence are maintained under `dev/`.

## 10. Project-specific Notes

Record additional information that is important for understanding or maintaining this project.

Do not turn this section into a development log or duplicate existing documentation.