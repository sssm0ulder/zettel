---
type: movie
aliases: "%"
---
%%cssClass: cards%%
## In process
```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	author AS "Director",
	parents AS "Category"
FROM !"templates"
WHERE type = "movie" AND status = "wip"
```
## To do

```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	author AS "Director",
	parents AS "Category"
FROM !"templates"
WHERE type = "movie" AND status = "todo"
```
## Done
```dataview
TABLE WITHOUT ID
	("![|80](" + cover + ")") as "Cover",
	file.link AS "Title",
	author AS "Director",
	parents AS "Category"
FROM !"templates"
WHERE type = "movie" AND status = "done"
```