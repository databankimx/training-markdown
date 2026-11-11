# 4. Links

A link has two parts: the text a reader sees, in square brackets, and the address, in round brackets, with no space between them:

~~~markdown
See the [employee portal](https://example.com/portal) for the policy.
~~~

~~~rendered
See the [employee portal](https://example.com/portal) for the policy.
~~~

The viewer shows the words "employee portal" as a link. A reader who clicks it goes to the address.

## Relative links

For a file in the same repository, use a relative path, which is the file's location from the document's own folder. A link from a file in a subfolder goes up one level with `../`:

~~~markdown
See the [setup script](../setup.ps1) for details.
~~~

~~~rendered
See the [setup script](../setup.ps1) for details.
~~~

Relative links keep working when the repository is copied or moved, because they don't depend on the machine they were written on. Use them for files in the same project.

## Link text

Make the link text say where the link goes. "Click here" tells the reader nothing, and it's hard to find in a long document:

~~~markdown
Read the [quickstart](QUICKSTART.md). Not: [click here](QUICKSTART.md).
~~~

~~~rendered
Read the [quickstart](QUICKSTART.md). Not: [click here](QUICKSTART.md).
~~~

## Images

An image uses the same pattern as a link, with an exclamation mark in front. The text in square brackets is the alt text, which describes the picture for anyone who can't see it, and which a viewer shows if the picture doesn't load. The address in round brackets is the file, using a relative path for a file in the project:

~~~markdown
![Runner window](docs/runner.png)
~~~

~~~rendered
![Runner window](docs/runner.png)
~~~

The runner doesn't load pictures in its rendered boxes, so you'll see the alt text, or a broken-picture marker, in place of the image. Your own viewer will show the picture.

Write alt text that says what the picture shows, not that it is a picture. "Runner window with the Check button" helps more than "Screenshot".

Keep image files in the repository beside the document that uses them. Git tracks them with the text, so the picture and its words stay in step. Git can't show what changed inside an image in a diff, though, so say what changed in the commit message.

## Try it

The starter has the first line of the page. Write the rest in the Source pane, so that the rendered page matches this description:

1. A paragraph that reads: The setup steps are in the quickstart. The word "quickstart" is a link to the file QUICKSTART.md.
2. A paragraph that reads: The policy is on the employee portal. The words "employee portal" are a link to https://example.com/portal.
3. A paragraph that reads: an image with the alt text Runner window, from the file runner.png.

The rendered page updates as you type. The check reports whether it matches the description too, and the link addresses count, so an address that's wrong or missing fails, even when the words are right.

Stuck? Press Show solution (spoiler) to see one correct answer, after you've tried.

> **Common mistake.** A space between the brackets and the parentheses, as in `[text] (address)`. The viewer shows the brackets as plain text, and no link is made.

---
