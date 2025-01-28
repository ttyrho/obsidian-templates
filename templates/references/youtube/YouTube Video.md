---
tags:
  - reference/youtube/video
type: YouTube Video
aliases:
channel:
playlist:
order:
authors:
date:
languages:
keywords:
classifiers:
collections:
---

# [Title](https://www.youtube.com/watch?v=<%tp.file.title%>)

## Content
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    order AS Time,
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
