# 5. Tables

A table uses pipes to separate the columns, and a row of hyphens under the header:

~~~markdown
| Language | Run command |
|---|---|
| C# | `dotnet run main.cs` |
| Python | `python main.py` |
| JavaScript | `node main.js` |
~~~

~~~rendered
| Language | Run command |
|---|---|
| C# | `dotnet run main.cs` |
| Python | `python main.py` |
| JavaScript | `node main.js` |
~~~

The first row is the header. The row of hyphens is required, and it's what makes the table a table. Each row needs the same number of columns as the header.

## Alignment

The row of hyphens can also set how a column is aligned. Put a colon at the left end of the hyphens for left alignment, at both ends for centered, and at the right end for right alignment:

~~~markdown
| Item | Quantity | Price |
|:---|:---:|---:|
| Coffee | 2 | 3.50 |
| Tea | 10 | 12.00 |
~~~

~~~rendered
| Item | Quantity | Price |
|:---|:---:|---:|
| Coffee | 2 | 3.50 |
| Tea | 10 | 12.00 |
~~~

This one table uses all three alignments: the item names are left-aligned, the quantities are centered, and the prices are right-aligned. Right alignment suits numbers, because the digits line up in their place value, so the two prices can be compared at a glance. Left is the default, so `---` on its own gives the same result as `:---`. Alignment is a small detail, so use it only where it helps the reader.

## Keep tables small

A table with more than four or five columns is hard to read in the source and in the preview. Use a list for longer content, or split the table into two.

## Leave a blank line before the table

A table that follows a paragraph needs a blank line between them, the same as a list. Without it, the viewer often joins the table to the paragraph, and the pipes show as plain text.

## Try it

The starter has the first line of the page. Write the rest in the Source pane, so that the rendered page matches this description:

1. A paragraph that reads: The tools and their versions:
2. A table with three columns, headed Tool, Required version, and Memory (GB), and three rows: Git, Any recent version, and 1; Node.js, 24 or later, and 2; Python, 3.12 or later, and 2. The Memory (GB) column is right-aligned.

The rendered page updates as you type. The check reports whether it matches the description. If the table doesn't appear, check the blank line before it.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** A row with a different number of pipes from the header. The viewer shows the row as text, or puts its cells in the wrong columns.

---
