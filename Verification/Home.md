# Automated Hardware/Software Verification

## Assignments
```dataview
TABLE due AS "Due Date", completed AS "Completed"
FROM "Verification/Assignments"
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
