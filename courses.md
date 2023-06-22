---
type: course
aliases: "{"
---

## In progress

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "course" AND status = "wip"
```

## To do

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "course" AND status = "todo"
```

## Done

```dataview
TABLE WITHOUT ID
	file.link AS "Title",
	url,
	category AS "Category"
FROM !"templates"
WHERE type = "course" AND status = "done"
```