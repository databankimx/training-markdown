---
applyTo: "**/*"
---

# GitHub Copilot Instructions - DataBank Development Standards

## Purpose
This file defines how GitHub Copilot should generate code for DataBank IMX development teams.
All generated code must align with internal standards for quality, maintainability, security, and consistency.

## Scope
This repository is a **Markdown training tutorial** with a small Electron lesson runner (`lesson-runner/`, plain JavaScript on Node.js). Follow the **Common Standards**, **Markdown Content Instructions**, and **JavaScript Project Instructions** sections for all generation in this repository.

---

## Common Standards

### General Principles
- Prioritize **readability, maintainability, and clarity** over brevity.
- Follow **DataBank coding standards** at all times.
- Assume code will be **reviewed, tested, and deployed to client environments**.
- Avoid unsafe, experimental, or non-production-ready patterns.
- Do not introduce unnecessary dependencies or frameworks.
- Third-party packages **must** have licenses that allow closed-source commercial use.
- Prefer existing project patterns over introducing new architectural or library choices.

### Architecture and Design
- Prefer clear separation of concerns.
- Avoid tightly coupled designs.
- Design for reuse and extensibility.
- Keep controllers, endpoints, and entry points thin; place business logic in services or domain components.
- Match the structure and conventions already used by the repository unless the user explicitly requests a redesign.

### Error Handling and Security
- Validate all inputs.
- Avoid exposing sensitive information in exceptions, logs, API responses, or console output.
- Follow least-privilege principles.
- Do not generate insecure defaults, hardcoded secrets, or bypass validation/authentication/authorization checks.
- Exception and error messages must be clear, concise, grammatically correct, and end with a period.

### Comments and Documentation
- Write comments only when necessary.
- Use clear, concise US-English.
- Document complex logic, non-obvious decisions, and important operational behavior.
- Avoid comments that merely restate the code.

### Source Control and Workflow
- All code must be tracked in source control.
- Commit early and often.
- Use meaningful commit messages.
- Link commits to tasks, issues, bugs, or enhancements where appropriate.
- Use branches and pull requests for review; do not commit directly to protected mainline branches.

### Code Reviews and Quality Gates
- All code must be reviewed before merge or delivery.
- Address correctness, readability, performance, security, and maintainability.
- Where applicable, code must pass SonarQube or other required quality gates before merge.

### Testing and QA Expectations
- Follow a **test-driven mindset** where practical.
- Ensure new code is testable.
- Include unit tests and integration tests where appropriate.
- Consider edge cases, invalid inputs, failure scenarios, and regression risk.

### Prohibited Practices
- Do NOT generate hardcoded credentials, secrets, tokens, or connection strings.
- Do NOT introduce unapproved third-party libraries.
- Do NOT expose internal implementation details unnecessarily.
- Do NOT produce code that violates DataBank IP, security, or delivery policies.

---

## Markdown Content Instructions

### Lessons and Documents
- Use hyphens, not em dashes. Use plain text symbols, not emojis.
- End each lesson with a horizontal rule.
- Use ATX headings (`#`), one H1 per file, and do not skip heading levels.
- Use fenced code blocks with a language name.
- Use clear link text and meaningful image alt text.
- Write in clear, concise US-English aimed at readers new to Markdown.

### Lesson Folder Structure
- Each lesson is a folder holding `lesson.json` and `lesson.md`.
- Exercises also have `starter.md`, `sample.md` (what the check compares with), and `solution.md`. The hint lives in `lesson.json`.
- Keep `sample.md` and `solution.md` consistent with the exercise description in `lesson.md`.
- Keep `README.md` and `QUICKSTART.md` in sync when lessons are added, renamed, or reordered.

### Shared Documents
- `development-rules-of-engagement.md` is shared across DataBank training repositories. Keep it in sync with the C# training repo and do not edit it casually.

---

## JavaScript Project Instructions (lesson-runner)

### General Style
- Write readable, idiomatic JavaScript for the Node.js version stated in `README.md`.
- Match the existing module layout under `lesson-runner/core/` and `lesson-runner/main.js`.
- Use descriptive names and prefer explicit code over clever code.
- Follow the repository's formatting and linting setup when present.

### Electron Security
- Keep `contextIsolation` enabled and `nodeIntegration` disabled in renderer windows.
- Do not load remote content or enable remote code execution.
- Validate any data crossing IPC boundaries, and validate paths read from lesson files.

### Error Handling and Logging
- Throw `Error` objects with clear messages that end with a period.
- Do not swallow errors silently, and preserve the original error as `cause` when wrapping.
- Never log secrets or personal data.

### Dependencies
- Install with `npm ci` and keep `package-lock.json` committed. Do not delete it to fix an install error.
- Pin versions and check licenses before adding any package.

### Testing
- No test framework is set up yet. If tests are added, prefer Node's built-in test runner unless the repository adopts another.

---

## Copilot Behavior Guidelines

When generating code, Copilot should:
- Follow all applicable rules in this document automatically.
- Prefer existing project patterns over new ones.
- Match surrounding code style closely.
- Avoid speculative implementations.
- Ask for clarification through comments or generated TODO notes only when requirements are genuinely unclear.

---

## Definition of Done

Generated code is acceptable only if it:
- Runs successfully without warnings in the target project context.
- Passes required static analysis and quality gates where applicable.
- Follows the Markdown and JavaScript standards in this file.
- Includes appropriate validation, error handling, and logging.
- Is readable, maintainable, and testable.
