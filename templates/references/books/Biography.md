---
tags:
  - reference/book/biography
type: Biography
aliases:
subjects:
authors:
date:
language:
keywords:
classifiers:
collections:
---

# [Title]()

## Content
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    page AS Page,
    type AS Type,
    keywords AS Keywords,
    collections AS Collections
FROM
    #literature/excerpt OR
    #literature/annotation
WHERE
    contains(reference, [[<%tp.file.title%>]])
SORT
    page ASCENDING,
    order ASCENDING
```
