# Markdown Basics

## License and Support

This repository is provided under the [MIT License](LICENSE). You are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell the materials in this repository, subject to the terms of that license.

This repository is provided for training and reference purposes only. DataBank IMX does not provide warranties, guarantees, maintenance, troubleshooting, implementation assistance, or technical support for this code or its use. Use it in any way permitted by the MIT License, but you are responsible for evaluating, adapting, testing, and supporting any use of it in your own environment.

## DataBank Responsibilities for Custom Code

All DataBank employees - including those working with AI-assisted tools - are bound by the [Development Rules of Engagement](development-rules-of-engagement.md). That document defines the rules for quoting, approving, developing, reviewing, scanning, storing, and delivering custom code for client work.

Key obligations that apply to everyone on every custom code engagement:

- **You own the code you deliver.** This applies equally to hand-written code, AI-assisted code, and AI-generated code. "The AI wrote it" is not an acceptable explanation for a production issue, a failed review, a security finding, or a support problem.
- **Code must be reviewed before delivery.** Review is interactive and must confirm that the code works, meets DataBank standards, is maintainable, and that the developer understands it well enough to explain, debug, and maintain it. Polished or well-formatted output - including AI-generated output - is not evidence of correctness.
- **Code must be in source control before delivery.** All custom code must be committed to the appropriate DataBank GitHub Enterprise repository before it is delivered to a client, regardless of whether the client receives source code, compiled binaries, or deployed functionality.
- **CI scanning must pass before delivery.** Required checks are the standards policy scan, SonarQube, and Snyk. A passing local build is not a substitute.
- **All third-party dependencies must be license-vetted.** The license must permit closed-source commercial use. Copyleft or unclear licensing must be escalated before use. Dependencies must not be added simply because an AI tool suggested them.
- **Only approved AI tools may be used.** Use only IT-approved tools through company accounts. All data entered into AI systems is subject to the [DataBank AI Acceptable Use Policy](https://workforcenow.adp.com/mascsr/wfncontenttools/file-management/file/JTJGc3RhdGljJTJGY2xpZW50cyUyRmNvbnRlbnQlMkZBSStBY2NlcHRhYmxlK1VzZStQb2xpY3kucGRmJTNGMTc3MTM0NzA4NjE4MQ==) and must be treated as confidential by default.
- **Custom code is billable work.** Code must be tied to an approved quote or engagement before commitment or delivery. Development quotes require approval from the Development Director or delegated development leadership before being sent externally.
- **Exceptions require explicit approval.** Time pressure alone is not a reason to bypass quote approval, source control, review, or CI scanning.

See the [Development Rules of Engagement](development-rules-of-engagement.md) for the full policy, including billing and quoting rules, source-code delivery rules, the delivery readiness checklist, and the exception process.

---

Markdown is plain text with a few marks that tell a viewer how to display it. You write headings with `#`, lists with `-`, and code in backticks, and the viewer turns those marks into headings, lists, and code blocks.

It's the format of the documents you'll read and write at work: READMEs, specifications, context documents, and notes. Changes to a Markdown file are tracked in source control just like changes to code, so a document can be reviewed the way code is. This short tutorial teaches the parts you'll use every day, and how to check a file before you share it.

## Quick start

The tutorial is at [databankimx/training-markdown](https://github.com/databankimx/training-markdown). Run the setup script once from the tutorial's folder, then start the runner. The script installs what's missing, including Git and Node.js, and it clones the repository if you run it from elsewhere:

```pwsh
powershell -NoProfile -ExecutionPolicy Bypass -File .\setup.ps1
cd lesson-runner
npm start
```

[QUICKSTART.md](QUICKSTART.md) has the details, including what the script installs, how the runner works, where your progress is saved, and how to fix common problems.

## What you need

- Windows 10 or 11
- Git, for cloning the repository
- Node.js 24 or later
- The Visual Studio Build Tools with the C++ workload, the fallback if Electron's download fails

The setup script installs anything that's missing. The Build Tools need an Administrator PowerShell.

You don't need any other program. The runner shows the Markdown you type and its rendered result side by side.

## The lessons

Work through them in order. Each lesson explains one part of Markdown, with examples shown in source and rendered. Most lessons end with an exercise: you type the Markdown in the Source pane, and the check tells you whether the rendered page matches the description. Spoiler solutions are available for every exercise, after you've tried.

0. **Why Markdown.** What Markdown is, and why it suits documents in a code repository, where changes are tracked like code. An introduction, with no exercise.
1. **Headings and paragraphs.** Headings, paragraphs, and line breaks, including the two-trailing-space line break. Exercise.
2. **Emphasis and inline code.** Bold, italics, bold and italics together, and code inside a sentence. Exercise.
3. **Lists.** Bulleted lists with a hyphen or an asterisk, numbered lists where every item can start with `1.`, and nested lists. Exercise.
4. **Links.** Links to pages and files, clear link text, and images with useful alt text. Exercise.
5. **Tables.** Tables, the blank line before them, and column alignment with colons. Exercise.
6. **Block quotes and rules.** Notes and asides, and horizontal rules. Exercise.
7. **Code blocks.** Fenced code blocks with a language name. Exercise.
8. **Checking a file before you share it.** A checklist for reviewing any Markdown file, with an exercise that fixes three common problems.
9. **Exercise: write a setup page.** Write the Markdown so that its rendered page matches a description.
10. **Summary.** The rules from every lesson, and a page to fix.

## The cheat sheet

Chapter 2, **Markdown Cheat Sheet**, is a one-page reference for the syntax in Chapter 1. It has no exercises.

## Conventions used in this tutorial

The lessons follow a few rules that make documents easier to review:

- Use hyphens, not em dashes.
- Use plain text symbols, not emojis.
- End each lesson with a horizontal rule.

These are good habits in any document, not only in this tutorial.

## Folder layout

- `setup.ps1` prepares the runner.
- `QUICKSTART.md` explains setup and the runner.
- `ch01-markdown-basics\` holds the lessons. Each lesson is a folder with `lesson.json` and `lesson.md`. Exercises also have a `starter.md`, a `sample.md` that the check compares with, a `solution.md` for the spoiler, and a hint in `lesson.json`.
- `ch02-markdown-cheat-sheet\` holds the cheat sheet.
- `lesson-runner\` is the runner: a desktop window built with Electron.

---

*Markdown Basics is a standalone tutorial. The AI-assisted coding course links to it from its context-documents and specifications chapters.*
