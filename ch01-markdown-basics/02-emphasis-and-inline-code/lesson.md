# 2. Emphasis and Inline Code

Emphasis changes how a word looks. Inline code shows a word or short piece of code exactly as written, in a monospace font.

## Bold and italics

Put two asterisks around text for **bold**, and one asterisk around it for *italics*:

~~~markdown
This is **bold**, and this is *italic*.
~~~

~~~rendered
This is **bold**, and this is *italic*.
~~~

To make text both bold and italic, use three asterisks on each side:

~~~markdown
This is ***bold and italic***.
~~~

~~~rendered
This is ***bold and italic***.
~~~

Some people use underscores, as in `__bold__` and `_italic_`. Pick one style and keep to it across a document. This course uses asterisks.

## Inline code

Put single backticks around a word or a short code fragment to show it as code:

~~~markdown
Call `parse_date` with the loan's due date.
~~~

~~~rendered
Call `parse_date` with the loan's due date.
~~~

Use inline code for file names, function names, commands, and anything a reader might type. A reader can see that `parse_date` is the name in the code, and not an ordinary word.

## Combining them

You can put emphasis around code, but keep it simple. A common pattern is to bold a label and show the value in code:

~~~markdown
**Expected:** `8 of 8 rows pass`
~~~

~~~rendered
**Expected:** `8 of 8 rows pass`
~~~

## Try it

The starter has the first line of the page. Write the rest in the Source pane, so that the rendered page matches this description:

1. A paragraph that reads: The build is ready and the output is in dist/. The word "ready" is bold. The text "dist/" is inline code.
2. A paragraph that reads: Review it before Friday. The word "before" is italic.

The rendered page updates as you type. The check reports whether it matches the description.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** Leaving out one of the two asterisks, which makes the rest of the line bold or italic. Check each pair when you preview.

---
