---
type: podcast
aliases: 
- "`"
---

## In progress
```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	podcast AS "Podcast",
	category AS "Category"
FROM !"templates"
WHERE type = "podcast" AND status = "wip"
```
## To do
```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	podcast AS "Podcast",
	category AS "Category"
FROM !"templates"
WHERE type = "podcast" AND status = "todo"
```
## Done
```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	podcast AS "Podcast",
	category AS "Category"
FROM !"templates"
WHERE type = "podcast" AND status = "done"
```