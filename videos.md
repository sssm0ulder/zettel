---
type: video
aliases: "$"
---

## In progress

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "video" AND status = "wip"
```
## To do

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "video" AND status = "todo"
```
## Done

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "video" AND status = "done"
```