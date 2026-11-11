# 6. Block Quotes and Rules

## Block quotes

A block quote starts with `>`. Use it for asides, notes, and warnings that you want to set apart from the main text:

~~~markdown
> **Note.** Save your work before you run the script.
~~~

~~~rendered
> **Note.** Save your work before you run the script.
~~~

A quote can run over several lines. Put a `>` at the start of each line, and a blank `>` line to separate paragraphs inside the quote:

~~~markdown
> **Aside: why the tests come first.**
> A test written after the code tends to check what the code does.
>
> A test written from the spec checks what the code should do.
~~~

~~~rendered
> **Aside: why the tests come first.**
> A test written after the code tends to check what the code does.
>
> A test written from the spec checks what the code should do.
~~~

The course uses block quotes for its asides. Keep them short, and use them for a note that's useful but not essential to the main point.

## Horizontal rules

Three hyphens on a line by themselves make a horizontal rule, a line across the page:

~~~markdown
---
~~~

~~~rendered
---
~~~

Use a rule to separate sections of a long document, or to mark the end of a lesson. Don't use rules between every paragraph. They stop being useful when there are too many.

Leave a blank line before and after a rule, so it isn't mistaken for a heading underline. A line of text directly above `---` can turn into a heading.

## Try it

The starter is empty. Write the page in the Source pane, so that the rendered page matches this description:

1. A block quote with a bold label Note., followed by the text: Save your work before you run the setup script.
2. A horizontal rule.
3. A paragraph that reads: Version 2 is ready.

The rendered page updates as you type. The check reports whether it matches the description.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** Writing a line of text directly above `---`. The viewer treats the text as a heading, which is rarely what you want.

---
