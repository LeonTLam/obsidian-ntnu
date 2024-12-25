---
tags:
  - Map
Maps: 
Bosses: 
Quests: 
Duration: 
Players: 
Enemies:
---

<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the concept a Title");
	await tp.file.rename(title);
} else {
	title = tp.file.title;
}

const parentFolder = "03_Current_Semester/Escape_From_Tarkov";

// Fetch the list of course folders
const courses = app.vault.getAbstractFileByPath(parentFolder).children.map(folder => folder.name);

// Prompt the user to select a course
const selectedCourse = await tp.system.suggester(courses, courses);

// Save the selected course to a variable or use it
let course = selectedCourse;

// Output the selected course or use it in your script
await tp.file.move("/01_Current_Semester/" + course + "/Assignments/" + title)
_%>

# Map

Image of Map

## Spawns

IMAGE of SPAWNS

## Extractions

IMAGE of EXTRACTIONS

Conditions to Extractions

## POIs


