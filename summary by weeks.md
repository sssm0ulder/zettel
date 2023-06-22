---
aliases: 
- "w" 
- "н"
---

# Задачи

```dataview
TASK
FROM "periodic/weekly"
WHERE !completed
GROUP BY file.link
```

## Summary по неделям

```dataview
TABLE WITHOUT ID
	file.link AS "Неделя",
	summary AS "Итог"
FROM "periodic/weekly"
WHERE summary
SORT file.name DESC
```

# Архив задач
```dataview
TASK
FROM "periodic/weekly"
WHERE completed
GROUP BY file.link
```