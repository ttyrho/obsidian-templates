---
tags:
  - reference/youtube/playlist
type: YouTube Playlist
aliases:
channel:
languages:
keywords:
collections:
---

# [Title](https://www.youtube.com/playlist?list=<%tp.file.title%>)

## Videos
```dataview
TABLE WITHOUT ID
	order AS Order,
	link(file.path, aliases[0]) AS Title,
	authors AS Speakers,
	channel AS Channel,
	date AS Date,
	languages AS Languages,
	keywords AS Keywords
FROM
	#reference/youtube/video
WHERE
	playlist = [[<%tp.file.title%>]]
SORT
	order ASCENDING
```
