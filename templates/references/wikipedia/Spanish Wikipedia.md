---
tags:
  - reference/wikipedia/spanish
type: Wikipedia
aliases:
date:
language: Spanish
keywords:
classifiers:
collections:
---

# [Title](https://es.wikipedia.org/wiki/<%tp.file.title%>)

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
