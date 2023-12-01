# Quarto Reprex: Listing chomps newlines

This site uses a custom listing with this template:

````markdown
```<%= item.codeLanguage %>
<%= item.code %>
```
````

and `post1.qmd` has YAML like this:

````markdown
---
title: "R code"

codeLanguage: r
code: |
  # Is there a line below this?

  fizz_buzz <- function(fbnums = 1:50) {
    # ...
  }

  # Is there a line above this?
---
````

When rendered, the newlines in `item.code` are lost.
