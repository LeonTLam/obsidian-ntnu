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

// Fetch the list of notes from selected course

const notesFolder = app.vault.getAbstractFileByPath(`${parentFolder}/${selectedCourse}/Notes`).children.map(folder => folder.name);

// Show a suggester to select a note
const selectedNote = await tp.system.suggester(notesFolder, notesFolder);

const subCourse = course.substring(0,7);

// Output the selected course or use it in your script
await tp.file.move("/01_Current_Semester/" + course + "/Concepts/" + title)

_%>
---
tags:
  - Concept
---
# Concept for <% "[[" + selectedNote + "]]" %>


