# {{title}}
## Tasks due today
```dataviewjs
dv.taskList(dv.pages().file.tasks
.where(t => !t.completed)
.where(t => t.text.includes("{{date:YYYY-MM-DD}}")))
```
## Log
