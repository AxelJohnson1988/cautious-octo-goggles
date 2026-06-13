# Contributing

Thank you for contributing to `cautious-octo-goggles`.

This repository is intended to support secure, governed, and maintainable autonomous intelligence systems. Contributions should improve the system without compromising security, auditability, or operational clarity.

## Contribution Principles

### Safety First

All proposed changes should be validated before review. At a minimum:
- Run the relevant test suite before opening a pull request
- Avoid introducing unbounded automation or unsafe defaults
- Document any security or compliance implications

### Deterministic Logic

Prefer predictable, reviewable, and transaction-safe designs over opaque or fragile behavior.

Examples:
- Favor explicit interfaces over hidden coupling
- Favor data validation and schema enforcement at boundaries
- Prefer durable state transitions over ad hoc mutation paths

### Documentation Required

Every material feature, fix, or architectural change should update the relevant documentation.

This may include:
- `README.md`
- files in `docs/`
- decision records in `docs/decision-records/`
- operational or security guidance affected by the change

### Conventional Commits

Use conventional commit messages where possible.

Examples:
- `feat: add policy evaluation hook`
- `fix: validate ingestion schema before processing`
- `docs: update architecture and operations guidance`
- `refactor: simplify orchestration task routing`

## Pull Request Expectations

Pull requests should be:
- Small enough to review effectively
- Clearly scoped
- Linked to the problem they solve
- Supported by tests when behavior changes
- Accompanied by documentation updates for material changes

## Coding Standards

When contributing code:
- Prefer modular design with single-responsibility components
- Avoid hardcoded secrets or environment-specific assumptions
- Centralize logging and error handling where practical
- Preserve traceability for security-relevant and compliance-relevant behavior
- Favor maintainable, explicit logic over clever shortcuts

## Testing Expectations

For code changes, include tests appropriate to the risk and scope of the change.

Focus on:
- Edge cases
- Failure behavior
- Authorization and policy behavior
- Input validation and error handling

## Security Reporting

If you identify a security issue, avoid publicly disclosing exploit details in an issue or pull request. Coordinate remediation through a private reporting path if one is established for the project.

## Architecture Decisions

Significant technical decisions should be documented in `docs/decision-records/` so future contributors understand the reasoning behind major choices.
