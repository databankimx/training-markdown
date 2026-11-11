# 8. Checking a File Before You Share It

Most Markdown mistakes look fine in the raw text and wrong in the preview, or the reverse. The fix is to check both, against the same short list, every time you share a file.

## The checklist

Work through these questions, in order, before you share a file.

**Structure**

- Is there one top-level heading, at the start?
- Do the lower headings nest in order, with no levels skipped?
- Is there a blank line before every list, table, quote, and rule?

**Content**

- Does every link go where you expect? Click each one in the preview.
- Does every table have the same number of columns in each row?
- Is every code block closed, and does it name its language?
- Is every bold or italic pair closed?

**Course rules**

- Are there any em dashes? Replace them with hyphens.
- Are there any emojis?
- Does the file end with a horizontal rule, if it's a lesson?

**Preview**

- Did you preview the file, not only read the source?
- Did anything you expected to be a heading, list, or table show as plain text?

## Run the same check on a whole folder

When you have many files, a search helps. In VS Code, use Find (Ctrl+F) to search the folder for the em dash character. Use Find in Files (Ctrl+Shift+F) to search every `.md` file at once.

For a larger course, a script is better. The AI-assisted coding course has one, `tools/check-course.js`, which checks its own files this way.

## Try it

The starter is a short project page with three problems. Fix them in the Source pane, so that the rendered page matches this description:

1. A top-level heading that says Project notes.
2. A paragraph that reads: Setup takes ten minutes, mostly waiting. Use a comma where the long dash is.
3. A bulleted list with two items: Install the tools, and Run the tests.

The rendered page updates as you type. The check reports whether it matches the description.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Aside: why a checklist beats memory.**
> The mistakes in this lesson are the ones an experienced writer makes too, because they're invisible when you're focused on the content. A checklist moves the check out of your head and onto the page, where it takes a minute and doesn't depend on how tired you are.

---
