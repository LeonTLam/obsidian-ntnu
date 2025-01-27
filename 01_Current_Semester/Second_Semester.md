# Semester: 🌸 Spring

---
## Courses:

- [[TTM4135|TTM4135 Anvendt Kryptografi ...]]
- [[TTM4115|TTM4115 Design av Kommuniserende systemer]]
- [[TDT4237|TDT4237 Programvaresikkerhet og Personvern]]
- [[PED3801|PED3801 Eksperter i team - VR/AR og AI for læring]]

---
## Deadlines:

### Assignments

```dataview
table course as "Course", 
      assignmentName as "Assignment Name", 
      (if(isGroupWork, "Group", "Individual")) as "Type", 
      dueDate as "Due Date", 
      isComplete as "Completed"
from "01_Current_Semester"
where contains(tags, "Assignment")
sort dueDate asc

```

### Exams

---
### Notes:
- Key goals for the semester.
- General reminders.