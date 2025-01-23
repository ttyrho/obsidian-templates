---
tags:
  - reference/book/monograph
type: Monograph
aliases:
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
    keywords AS Keywords
FROM
    #literature/excerpt OR
    #literature/annotation
WHERE
    contains(reference, [[<%tp.file.title%>]])
SORT
    page ASCENDING,
    order ASCENDING
```

## Exercises
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    page AS Page,
    solved AS Solved,
    keywords AS Keywords,
    collections AS Collections
FROM
    #literature/exercise
WHERE
    contains(reference, [[<%tp.file.title%>]])
SORT
    page ASCENDING,
    order ASCENDING
```
