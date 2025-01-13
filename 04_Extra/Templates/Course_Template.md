<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the Course a Title");
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

const subCourse = course.substring(0,7);

// Output the selected course or use it in your script
await tp.file.move("/01_Current_Semester/" + course + "/" + course + " " + title)

_%>

# General Information
- **Course Code**: `<% subCourse %>`
- **Institution**: `NTNU`
- **Program**: `Digital Infrastructure and Cybersecurity`
- **Credits**: `7.5 ECTS`
- **Semester**: `Spring 2024`

---

## Course Description
`Provide a brief overview of the course, including its purpose and key objectives. Mention the skills or knowledge students are expected to gain.`

---

## Topics Covered
- `Topic 1`
- `Topic 2`
- `Topic 3`
- `...`

---

## Learning Objectives
By the end of this course, students should be able to:
1. `Objective 1`
2. `Objective 2`
3. `Objective 3`

---

