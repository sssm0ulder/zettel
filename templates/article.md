<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
title = await tp.system.prompt("Title");
}
await tp.file.rename(title)
-%>---
type: article
aliases: 
- "; <%* tR += title %>"
status: todo
recommendedby:
---
___
tags:: 
prev:: [[articles|Back to articles library]]
category::
url::
children::
___
PDF

<% tp.file.cursor(0) %>