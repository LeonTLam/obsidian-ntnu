<%*
// Give file title
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the Assignment a Title");
	await tp.file.rename(title);
} else {
	title = tp.file.title;
}

// Give assignment a due date

const selectedDate = await tp.system.prompt("Select a date (YYYY-MM-DD):"); 

// Define the parent folder containing courses
const parentFolder = "01_Current_Semester";

// Fetch the list of course folders
const courses = app.vault.getAbstractFileByPath(parentFolder).children.map(folder => folder.name);

// Prompt the user to select a course
const selectedCourse = await tp.system.suggester(courses, courses);

// Save the selected course to a variable or use it
let course = selectedCourse;

const subCourse = course.substring(0,7);

// Output the selected course or use it in your script
await tp.file.move("/01_Current_Semester/" + course + "/Assignments/" + title)

_%>
---
dueDate: <% selectedDate %>
course: "<% "[[" +subCourse+ "]]" %>"
isGroupWork: 👨‍👩‍👧‍👦 Group👨‍🦯‍➡️Individual
Status: 🛑 Not Started
tags:
  - Assignment
assignmentName: "<% title %>"
---
```meta-bind-embed
[[META_WORKTYPE]]
```
```meta-bind-embed
[[META_QUEST]]
```
# Assignments for <% "[[" +subCourse+ "]]" %>

### Details:
- **Description:**
  - Brief description of the assignment.

### Notes:
- Any specific notes about the assignment.