# Markdown Cheat Sheet

A one-page reference for the syntax in Chapter 1. Use it while you write, and go back to the lesson when a rule isn't clear.

## Text

| You want | Write | Notes |
|---|---|---|
| A top-level heading | `# Title` | One per document, at the top |
| A section heading | `## Section` | Then `###`, `####`, and so on, without skipping |
| A paragraph | Text, then a blank line | Lines with no blank line between them join |
| Bold | `**word**` | Two asterisks on each side |
| Italics | `*word*` | One asterisk on each side |
| Inline code | `` `name` `` | For file names, commands, and code words |

## Lists

| You want | Write | Notes |
|---|---|---|
| A bulleted list | `- item` | A blank line before the list |
| A numbered list | `1. item` | Numbers can be in order or all `1.` |
| A nested list | Indent the sub-items | Indent under the item they belong to |

## Links, tables, and quotes

| You want | Write | Notes |
|---|---|---|
| A link to a page | `[text](https://example.com)` | Clear text, no space in the middle |
| A link to a file | `[text](docs/setup.md)` | Relative to the current file |
| An image | `![alt text](docs/runner.png)` | Like a link, with an exclamation mark in front. The alt text describes the picture |
| A table | Header row, then `\|---\|---\|`, then rows | Every row has the same number of columns |
| Column alignment | `:---` left, `:---:` centered, `---:` right | In the row of hyphens. Right-align numbers |
| A block quote | `> text` | `>` at the start of each line |
| A horizontal rule | `---` | On its own line, with a blank line around it |

## Code blocks

Put three backticks on a line, add the language name, write the code, and close with three backticks on a line of their own. Use three tildes instead when the block shows Markdown, so its backticks don't close it.

## Before you share a file

- Read the source, then the rendered page.
- Check the heading levels and the blank lines before lists and tables.
- Check that every link goes where you expect.
- Check that every bold and italic pair is closed.
- Check that the file has no em dashes.
