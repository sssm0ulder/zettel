---
type: article
aliases: ";"
---

## Work in progress
```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	link,
	category AS "Category"
FROM !"templates"
WHERE type = "article" AND status = "wip"
```
## To do
```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	link,
	category AS "Category"
FROM !"templates"
WHERE type = "article" AND status = "todo"
```
## Done
```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	link,
	category AS "Category"
FROM !"templates"
WHERE type = "article" AND status = "done"
```