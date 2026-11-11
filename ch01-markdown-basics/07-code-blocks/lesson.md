# 7. Code Blocks

Inline code, from lesson 2, is for a few words. A code block is for several lines. It's a fence: three backticks on their own line, the code, then three backticks to close it.

~~~markdown
```python
def is_even(n):
    return n % 2 == 0
```
~~~

~~~rendered
```python
def is_even(n):
    return n % 2 == 0
```
~~~

## Naming the language

Put the language name after the opening fence, as in `python` above. The viewer uses it to color the code. Common names are `csharp`, `python`, `javascript`, `powershell`, `markdown`, and `text`.

If you don't know the language, or the block is plain output, use `text`. Don't leave the name out for code that has a language, because a block with no name is shown as plain text with no coloring.

## Showing Markdown inside Markdown

A problem comes up when the block you want to show contains backticks. A three-backtick fence inside another three-backtick fence closes the outer block early. Two ways around it:

- Use a fence of four backticks for the outer block, which the inner three-backtick fence can't close.
- Use three tildes (`~~~`) for the outer block, as this lesson does.

Both work. Pick one, and use it the same way throughout a document.

## Try it

The starter is empty. Write the page in the Source pane, so that the rendered page matches this description:

1. A code block with the language python, containing two lines: def is_even(n): and then, indented by four spaces, return n % 2 == 0
2. A code block with the language text, containing one line: 2 is even

The rendered page updates as you type. The check reports whether it matches the description.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** Forgetting the closing fence. Every line after it, to the end of the file, shows as code.

---
