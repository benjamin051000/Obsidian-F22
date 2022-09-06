# Automated Hardware/Software Verification
[Canvas](https://ufl.instructure.com/courses/465733)
[[syllabusEEL47015702.pdf]]
Contact: tuba@ece.ufl.edu
Office Hours: Tuesday @ #todo

# Assignments
```dataview
TABLE due AS "Due Date 📅", choice(Tasks.completed, "Done ✅", "Not done") AS "Status ✔"
FROM "Verification/Assignments"
SORT due DESC
```

***
## To Do 📑
```dataview
TASK
FROM "Verification/Assignments"
GROUP BY file.link
SORT due DESC
```

# Lecture Notes
```dataview
TABLE date AS "Date"
FROM #ver/lecture 
SORT date DESC
```
