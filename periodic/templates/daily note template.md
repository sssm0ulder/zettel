- <% tp.file.cursor(0) %>

#### Заметки сделанные в этот день
```dataview
LIST
WHERE file.cday = date(<% tp.file.title %>)
```