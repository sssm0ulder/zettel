---
type: book
aliases: "&"
---
%%cssClass: cards%%

## In progress

```dataview
TABLE WITHOUT ID
   ("![|80](" + cover + ")") as "Cover",
   file.link AS "Title",
   author AS "Author(s)",
   start AS "Started",
   category AS "Category"
FROM !"templates"
WHERE type = "book" AND status = "wip"
```

## To do

```dataview
TABLE WITHOUT ID
   ("![|80](" + cover + ")") as "Cover",
   file.link AS "Title",
   author AS "Author(s)",
   start AS "Started",
   category AS "Category"
FROM !"templates"
WHERE type = "book" AND status = "todo"
```

## Done 

```dataview
TABLE WITHOUT ID
   ("![|80](" + cover + ")") as "Cover",
   file.link AS "Title",
   author AS "Author(s)",
   start AS "Started",
   end AS "Ended",
   category AS "Category"
FROM !"templates"
WHERE type = "book" AND status = "done"
```