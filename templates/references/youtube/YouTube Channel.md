---
tags:
  - reference/youtube/channel
type: YouTube Channel
aliases:
languages:
keywords:
collections:
---

# [Title](https://www.youtube.com/<%tp.file.title%>)

## Playlists
```dataview
TABLE WITHOUT ID
	link(file.path, aliases[0]) AS Title,
	keywords AS Keywords
FROM
	#reference/youtube/playlist
WHERE
	channel = [[<%tp.file.title%>]]
```

## Videos
```dataview
TABLE WITHOUT ID
	link(file.path, aliases[0]) AS Title,
	playlist AS Playlist,
	authors AS Speakers,
	date AS Date,
	languages AS Languages,
	keywords AS Keywords
FROM
	#reference/youtube/video
WHERE
	channel = [[<%tp.file.title%>]]
SORT
	date DESCENDING
```
