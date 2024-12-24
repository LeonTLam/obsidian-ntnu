<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the concept a Title");
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
await tp.file.move("/01_Current_Semester/" + course + "/Concepts/" + title)

_%>

## Definition:
- Brief definition or description.

## Key Details:
- Point 1
- Point 2

## Examples:
1. Example 1.
2. Example 2.

