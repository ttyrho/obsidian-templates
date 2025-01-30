---
tags:
  - catalog/conference
aliases:
date:
place:
---

# <%tp.file.title%>

## Papers
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    authors AS Authors,
    language AS Language,
    keywords AS Keywords,
    classifiers AS Classifiers,
    collections AS Collections
FROM
    #reference/research/paper
WHERE
    contains(conference, [[<%tp.file.title%>]])
```
