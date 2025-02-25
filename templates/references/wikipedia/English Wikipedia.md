---
tags:
  - reference/wikipedia/spanish
type: Wikipedia
aliases:
date:
language: English
keywords:
classifiers:
collections:
---

# [Title](https://en.wikipedia.org/w/index.php?title=Tensor_product<%tp.file.title%>&oldid=)

## Content
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    type AS Type,
    keywords AS Keywords
FROM
    #literature/excerpt OR
    #literature/annotation
WHERE
    contains(reference, [[<%tp.file.title%>]])
SORT
    order ASCENDING
```
