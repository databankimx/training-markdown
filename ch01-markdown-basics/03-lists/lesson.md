# 3. Lists

Lists are the most common structure in the documents you'll write. Markdown has two kinds, bulleted and numbered, and you can nest either one.

## Bulleted lists

Start each item with a hyphen and a space:

~~~markdown
- Read the spec
- Write the acceptance table
- Check each row by hand
~~~

~~~rendered
- Read the spec
- Write the acceptance table
- Check each row by hand
~~~

Use a bulleted list when the order doesn't matter, such as a list of requirements or constraints.

You can start a bulleted item with a hyphen or an asterisk. Both make the same list, so pick one and keep to it across a document.

~~~markdown
* Read the spec
* Write the acceptance table
~~~

~~~rendered
* Read the spec
* Write the acceptance table
~~~

## Numbered lists

Start each item with a number and a full stop. The numbers don't need to be in order, because the viewer renumbers them, but writing them in order makes the source easier to read:

~~~markdown
1. Classify the data.
2. Write the spec.
3. Run the tests.
~~~

~~~rendered
1. Classify the data.
2. Write the spec.
3. Run the tests.
~~~

Use a numbered list when the order matters, such as the steps of a procedure.

You don't need to count the items yourself. Write `1.` at the start of every item, and the renderer numbers them in order. Writing 1, 2, 3 is also fine, and it's easier to read in the source.

~~~markdown
1. Classify the data
1. Write the spec
1. Run the tests
~~~

~~~rendered
1. Classify the data
1. Write the spec
1. Run the tests
~~~

## Nested lists

Indent the sub-item by two or four spaces, and start it with a hyphen:

~~~markdown
1. Write the spec.
   - Name the inputs.
   - Name the errors.
2. Write the tests.
~~~

~~~rendered
1. Write the spec.
   - Name the inputs.
   - Name the errors.
2. Write the tests.
~~~

Keep nesting to two levels where you can. Deeper lists are hard to read in the source and in the preview.

## Lists with a paragraph

Leave a blank line before a list that follows a paragraph, so the viewer knows the list starts there. That's the most common reason a list shows as plain text.

## Try it

The starter has the first line of the page. Write the rest in the Source pane, so that the rendered page matches this description:

1. A numbered list with three items: Clone the repository, Install the packages, and Open the runner.
2. Under the second item, a bulleted list with two items: Run npm ci, and Run npm test.

The rendered page updates as you type. The check reports whether it matches the description.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** A list that runs straight on from a paragraph, with no blank line. The preview shows the hyphens as text, and the list doesn't start.

---
