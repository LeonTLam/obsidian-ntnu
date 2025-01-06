<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the Daily Note a Title");
	await tp.file.rename(title);
} else {
	title = tp.file.title;
}

// Define the parent folder containing courses
const parentFolder = "01_Current_Semester";

// Fetch the list of course folders
const courses = app.vault.getAbstractFileByPath(parentFolder).children.map(folder => folder.name);

// Prompt the user to select a course
const selectedCourse = await tp.system.suggester(courses, courses);

// Save the selected course to a variable or use it
let course = selectedCourse;

// Output the selected course or use it in your script
await tp.file.move("/01_Current_Semester/" + course + "/Notes/" + title)

_%>
# <% tp.date.now("DD-MMM-YYYY") %> Daily Note for <% "[[" +course+ "]]" %>

## Topics Covered
- Topic 1
- Topic 2

## Key Points
- Summary of key discussions.

## Notes
- Additional notes or reminders.

---

Created on <% tp.date.now("DD-MMM-YYYY HH:mm") %>
