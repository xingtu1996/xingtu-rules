# XingTu Rules · Engineering AI Collaboration Rules

[简体中文](./README.md) | **English**

> A reusable, source-readable rule library for AI-assisted engineering. This is primarily a **rules and methodology repository**, not an autonomous enforcement engine.

[![License: MIT](https://img.shields.io/badge/license-MIT-informational)](./LICENSE)

## Purpose

`xingtu-rules` explores how coding guidelines, workflow constraints, and review expectations can be expressed as rules that people and AI coding agents can inspect. The repository favors explainable, scoped, composable and versionable instructions.

- **Global rules:** reusable guidance maintained in [`rules/`](./rules/).
- **Scoped rules:** guidance selected for a project or directory, with concrete integration still under development.
- **On-demand rules:** planned patterns for loading only task-relevant instructions.
- **Self-description:** see [the repository contract](./SELF.md) and [the eight-field architecture](./docs/architecture.md).

**Implemented vs planned:** The repository currently includes the engineering meta-rule and documentation. It does **not** claim that every proposed rule layer has been populated, that every agent supports the same rule-loading conventions, or that rule files impose hard security permissions.

## Getting started

1. Read [`rules/engineering-rules.md`](./rules/engineering-rules.md).
2. Read the relevant coding agent's official instructions/loading mechanism: [reference index](./docs/references/coding-agents.md).
3. Review your target project's existing `AGENTS.md`, `CLAUDE.md`, and any project-scoped instructions.
4. Select only the rules that apply, review conflicts, and add them explicitly to your agent's supported location.
5. Test the effective behavior in that target agent and record the result. Copying a file alone is **not** evidence that an agent loaded or enforced it.

```sh
# Inspect the available engineering meta-rule
cat rules/engineering-rules.md
```

## Architecture and evidence

- [Project self-description](./SELF.md)
- [Architecture and self-description contract](./docs/architecture.md)
- [Ecosystem and integration boundaries](./docs/ecosystem.md)
- [Research references](./docs/references/research.md)
- [Coding-agent documentation references](./docs/references/coding-agents.md)
- [Validation notes](./docs/XRULE-001-report.md)

**DeepSeek Harness / DSH:** Its instruction-loading behavior and the loading behavior of other agents differ. An automatic Rules adapter is **not verified** here; runtime integration is **NOT_RUN**. This project is independent and is not an official DeepSeek repository.

## Where this fits in XingTu

| Project | Responsibility |
| --- | --- |
| [XingTu AI Engineering](https://github.com/xingtu1996/xingtu-ai-engineering) | Broader AI engineering methods |
| [XingTu Skills](https://github.com/xingtu1996/xingtu-skills) | Reusable task skills |
| [XingTu Hooks](https://github.com/xingtu1996/xingtu-hooks) | Tool-execution guardrails, where supported |
| [XingTu SDD](https://github.com/xingtu1996/xingtu-sdd) | Spec-driven design and acceptance |
| [XingTu Harness](https://github.com/xingtu1996/xingtu-harness) | Aggregation and installation, subject to compatibility tests |
| [XingTu profile](https://github.com/xingtu1996) | Public repository navigation |

Links are for discovery; they do not automatically install, inherit, or activate rules across repositories.

## Contributing and security

Please describe the problem, target agent/version, actual loading mechanism, reproduction steps, and observed results. Do not submit personal, customer, employer, secret, or private workspace materials. Mark untested designs as such; do not present proposals as operational features.

## License

This repository contains an [MIT License](./LICENSE). External content and brands remain subject to their respective owners' rights.

## About

XingTu (行途) — hands-on AI engineering and reusable developer practices. See [GitHub](https://github.com/xingtu1996) for other projects and updates.
