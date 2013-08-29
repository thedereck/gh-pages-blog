---
layout : post
title : How to get code to format correctly
category : Tutorial
tags :
  - tutorial
---

I recently received a quesiton about how to get code to render correctly on a blog post. In order to get the code to render, you'll need to wrap it in ````` and include a blank line before the code block.

For example:

```
function code_example() {
  console.log("Showing the rendering of code using gh-pages-blog.");
}
```

In order to turn on syntax highlighting, you'll also need to include the language in the first line:

```javascript
function code_example_with_highlights() {
  console.log("Showing the rendering of code using gh-pages-blog.");
}
```

For a complete list of supported programming languages, see the [languages.yml](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml) file provided by the [Linguist](https://github.com/github/linguist) project.

Dereck
