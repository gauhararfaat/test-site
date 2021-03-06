---
id: doc5
title: Fifth Document
---

Docusaurus supports some extra features when writing documentation in markdown.

### Linking other Documents

You can use relative urls to other documentation files which will automatically get converted to the corresponding html links when they get rendered.

Example:
```
[This links to another document](/docs/en/other-document.md)
```
If the permalink in the header of `other-document.md` is `/docs/en/other-document.html`, this markdown will automatically get converted into a link to `/docs/en/other-document.html` once it gets rendered.

This can help when you want to navigate through docs on GitHub since the links there will be functional links to other documents (still on GitHub), but the documents will have the correct html links when they get rendered.

### Generating Table of Contents

You can make an autogenerated list of links, which can be useful as a table of contents for API docs.

In your markdown file, insert a line with the text <`AUTOGENERATED_TABLE_OF_CONTENTS>`. Write your documentation using `h3` headers for each function inside a code block. These will be found by Docusaurus and a list of links to these sections will inserted at the text <`AUTOGENERATED_TABLE_OF_CONTENTS>`.

Example:
```markdown
### `docusaurus.function(a, b)`

Text describing my function


### `docdoc(file)`

Text describing my function
```

will lead to a table of contents of the functions:

```
- `docusaurus.function(a, b)`
- `docdoc(file)`
```
and each function will link to their corresponding sections in the page.
