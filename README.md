# Markdown Basics

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
