# 1. Headings and Paragraphs

A heading starts with one or more `#` signs, then a space, then the heading text. One `#` is the top level, and each extra `#` makes a smaller level below it.

~~~markdown
# Top level

## Second level

### Third level
~~~

The example's heading is shown one level smaller below, so it fits inside this lesson.

~~~rendered
## Top level

### Second level

#### Third level
~~~

Use one top-level heading per document, at the start. Use the lower levels to divide the document into sections. Don't skip levels, such as going from `#` straight to `###`, because some viewers and tools use the levels to build a table of contents.

## Paragraphs

A paragraph is one or more lines of text, followed by a blank line. Line breaks inside a paragraph don't start a new paragraph in the viewer:

~~~markdown
This sentence and the next one
sit in the same paragraph.

This is a new paragraph.
~~~

~~~rendered
This sentence and the next one sit in the same paragraph.

This is a new paragraph.
~~~

The viewer shows the two lines of the first paragraph as one. Leave a blank line between paragraphs.

## A line break without a new paragraph

Sometimes you want a line to end where you put it, without starting a new paragraph. End the line with two trailing spaces, and the viewer breaks the line there, but keeps the text in the same paragraph. This is a non-paragraph line break.

~~~markdown
First line, with two trailing spaces  
second line, in the same paragraph.
~~~

~~~rendered
First line, with two trailing spaces  
second line, in the same paragraph.
~~~

Trailing spaces are invisible in most editors, so check the preview, not only the source. A backslash at the end of a line also works in many viewers, but two spaces is the form most tools share.

## Try it

The starter has the first line of the page. Write the rest in the Source pane, so that the rendered page matches this description, part by part:

1. A second-level heading that says Decisions.
2. One paragraph that reads: We will ship on Friday if the tests pass. Write it on two lines. The line break can fall anywhere inside the sentence, or there can be no line break at all. What matters is that the sentence is one paragraph, with no blank line inside it.
3. A second paragraph that reads: The review is on Monday.

The rendered page updates as you type. The check reports whether it matches the description, and if it doesn't, the hint explains the rule to check.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** Starting a heading without the space, as in `#Notes`. Many viewers show that as plain text, not a heading. Always leave a space after the `#` signs.

---
