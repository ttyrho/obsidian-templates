---
tags:
  - catalog/keyword
aliases:
keywords:
---

# <%tp.file.title%>

## Keywords
```dataview
TABLE WITHOUT ID
    file.link AS Name
FROM
    #catalog/keyword
WHERE
    contains(keywords, [[<%tp.file.title%>]])
SORT
    file.name
```

## References
```dataview
TABLE WITHOUT ID
    link(file.path, file.aliases[0]) AS Title,
    authors AS Authors,
    date AS Date,
    language AS Language,
    collections AS Collections
FROM
    #reference
WHERE
    contains(keyword, [[<%tp.file.title%>]])
SORT
    date DESCENDING
```

## Knowledge
```dataview
TABLE WITHOUT ID
    file.link AS Title,
    type AS Type,
    keywords AS Keywords,
    collections AS Collections
FROM
    #knowledge
WHERE
    contains(keywords, [[<%tp.file.title%>]])
```

## Literature
```dataview
TABLE WITHOUT ID
    file.link AS Title,
    type AS Type,
    reference AS Reference,
    keywords AS Keywords,
    collections AS Collections
FROM
    #literature
WHERE
    contains(keywords, [[<%tp.file.title%>]])
```
