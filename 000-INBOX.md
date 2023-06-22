
---
aliases: 
- "поиск несвязанных заметок"
- "inbox"
- "atom"
- "orphan"
tags: 📥
---
# 📥 inbox

```dataview
LIST
FROM #📥 and !"templates"
WHERE 
file.link != [[000-INBOX]]
```

# ⚛ Pending atomization

```dataview
LIST
FROM #⚛ 
```

# 💔 Orphan

Здесь приводится **LIST** из *заметок* и *файлов*, которые ни с чем НЕ связаны:

```dataview
LIST
FROM 
	!"home" 
	AND 
	!"templates" 
	AND 
	!"periodic/daily" 
	AND 
	!"periodic/weekly"
	AND 
	!"periodic/templates"  
	AND 
	!"files/excalidraw"
	AND 
	!"files"
	AND
	!"projects"
WHERE
	length(file.inlinks) = 0 
	AND 
	length(file.outlinks) = 0 
	AND 
	file.link != [[excalibrain]]
	AND
	file.link != [[excalidraw_template]]
```
