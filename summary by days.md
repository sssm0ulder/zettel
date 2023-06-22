---
aliases: 
- "d" 
- "д"
- "в"
---

# ✔Задачи

```dataview
TASK
FROM "periodic/daily"
WHERE !completed
GROUP BY file.link
```

# Идеи

```dataview
TABLE WITHOUT ID
	file.link AS "День",
	idea AS "Идея"
FROM "periodic/daily"
WHERE idea
```

# Архив задач

```dataview
TASK
FROM "periodic/daily"
WHERE completed
GROUP BY file.link
```