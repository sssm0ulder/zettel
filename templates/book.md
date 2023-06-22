<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
title = await tp.system.prompt("Title");
}
await tp.file.rename(title)
-%>---
type: book
aliases: 
- "& <%* tR += title %>"
cover: {{coverUrl}}
start:
end:
status: todo
recommendedby:
---
___
tags:: 
prev:: [[books|Back to library]]
category::
author:: [[{{author}}]]
children::
author::
___
PDF
![cover|150]({{coverUrl}})
___

<% tp.file.cursor(0) %>