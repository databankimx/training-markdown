# Why Markdown

Before you write anything, it helps to know what Markdown is, where you'll meet it, and why so many of the documents in a software project are written in it. This lesson covers that, and it's written in Markdown too, so you're already reading it. The rest of the tutorial is the practice.

## What Markdown is

Markdown is a way of writing formatted text using ordinary characters. You don't click a button to make a heading. You type a `#` in front of the words, and a viewer draws the heading.

~~~markdown
# Setup

Install the tools in this order:

- Git
- Node.js 24
- The lesson runner
~~~

Read that as plain text, and you can already tell what it means. A viewer that understands Markdown turns it into a heading, a paragraph, and a bulleted list. A viewer that doesn't understand it still shows the marks, so the text stays readable.

That second part is deliberate. Markdown is designed so that the source reads well as it stands. You don't need a special program to open it, and you can read it in a terminal, a diff, or an email.

~~~rendered
### Setup

Install the tools in this order:

- Git
- Node.js 24
- The lesson runner
~~~

The example's top-level heading is shown one level smaller here, so it fits inside this lesson.

## Where you'll meet it

Markdown is everywhere developers work, often without anyone mentioning it:

- **README files.** The first page of most software projects, shown on the repository's front page.
- **Issues and pull requests.** The comment boxes on most code hosting sites accept Markdown.
- **Documentation sites.** Many are built from Markdown files kept in the repository.
- **Chat and notes.** Many chat tools and note apps understand the same basic marks.
- **Specifications and design notes.** Plain files that describe what a piece of software should do, and why.

Learn the basics once, and you can write in all of these places.

## Source and rendered

A Markdown file has two forms. The source is what you type: the `#`, the hyphens, the backticks. The rendered page is what a viewer draws from it, with real headings, lists, and code blocks.

Good Markdown works in both forms. The source is easy to read and edit, and the rendered page is easy to scan. You'll often check both: the source to see the marks are right, and the rendered page to see the result. The runner in this tutorial shows both side by side, so you can do that as you work.

> **Aside: why not HTML?**
> HTML can express everything Markdown can, and more. But its source is full of tags, such as `<h1>` and `<p>`, that get in the way of reading the words. Markdown trades some of that power for source that a person can read at a glance. For documents, that trade is usually the right one.

## Why it suits documents in a code repository

A code repository holds more than code. It holds the README, the setup instructions, the specifications, the design notes, and the record of decisions and why they were made. Most of those documents are in Markdown, for three reasons.

**They're plain text.** Git, the tool most teams use for source control, is built to track plain text. It can show you exactly what changed in a plain-text file, line by line.

**They're reviewed like code.** A change to a Markdown file goes through the same review as a change to a program. A colleague reads the change, comments on it, and approves it before it's merged.

**They stay with the code.** A document in the repository is in the same version as the code it describes. When you check out an older version of the project, you get the documents from that time as well.

## Changes are tracked, just like code

This is the advantage that matters most in practice. Every change to a Markdown file is recorded in source control, with who made it, when, and why. You can see the history of any line, and you can undo any change.

Suppose someone updates the setup instructions. Git shows the change as a diff, which lists the lines removed and the lines added:

~~~diff
 ## Requirements
 
-- Node.js 20 or later
+- Node.js 24 or later
- Git
~~~

A line with a minus sign was removed, a line with a plus sign was added, and the unchanged lines around them give the context. A reviewer can read that in seconds and decide whether the change is right.

Compare that with a Word document. Word stores the file as a binary package, so a diff of two versions tells you only that the file changed. You can't see what changed without opening both copies and comparing them by eye. Many teams have lost a day to a Word file that was edited in two places, because no tool could merge the two versions cleanly.

With Markdown, the same two versions merge the way code does. If two people edit different lines, Git combines both changes automatically. If they edit the same line, Git marks the conflict, and the people involved resolve it in the file itself.

> **Aside: why the diff is the document's audit trail.**
> When a decision changes, the reason is often in the diff, in the commit message, or in the review comment on the change. A wiki page usually shows only the current text. A Markdown file in a repository keeps the whole history of the decision, next to the code it affects.

## What Markdown is not good for

Markdown is a good fit for text with light structure. It's a poor fit for some things:

- **Precise layout.** A flyer, a slide deck, or a page where the position of each element matters.
- **Large or complex tables.** Tables with many columns or merged cells are hard to write and hard to read in source.
- **Data.** A spreadsheet or a dataset belongs in a file made for it, such as CSV, not in a document.

When you need one of these, use the right format, and link to it from the Markdown document.

## What this means for you

Because your documents live next to the code, write them as you would write code. Keep each change small and focused, so the diff is easy to read. Describe the reason for the change in the commit message. Ask for a review, as you would for code.

Markdown also keeps the documents open to everyone on the team. Anyone can read the source, and anyone who can review a change can review a document.

## What you'll learn in this tutorial

The next lessons teach the parts of Markdown you'll use every day: headings, emphasis, lists, links and tables, block quotes, and code blocks. The lesson after them is a checklist for reviewing a Markdown file before it's shared, which is the same habit as reviewing a change to code. The last step is an exercise, where you write a short document to match a description.

Each lesson has a practice task, and the runner lets you type Markdown and see the rendered result beside it. Once you can write a document that reads well as source and as a rendered page, you can write for a repository.

---
