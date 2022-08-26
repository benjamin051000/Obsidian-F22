# Automated Hardware/Software Verification

## Assignments
```dataview
TABLE due AS "Due Date", choice(Tasks.status, "done", "not done") AS Status
FROM "Verification/Assignments"
WHERE file.tasks
SORT due DESC
```

***

```dataview
TASK
FROM "Verification/Assignments"
GROUP BY file.link
SORT due DESC
```

## Lecture Notes
```dataview
TABLE date AS "Date"
FROM #ver/lecture 
SORT date DESC
```
