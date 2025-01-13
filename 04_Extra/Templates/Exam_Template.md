<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the Exam a Title");
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
await tp.file.move("/01_Current_Semester/" + course + "/Exams/" + title)

_%>


#### **Exam Details**

- **Title**: [Enter Exam Title]
- **Course**: **<% "[[" + subCourse + "]]" %>**
- **Due Date**: [Enter Due Date]
- **Description**: [Provide a brief description of the exam, including its purpose, format, and any important details.]

---

#### **Progress**

- [ ] Review notes from lectures 🔽
- [ ] Practice past exams 🔼 
- [ ] Create a summary of key topics 🔼 


---

#### **Topics**

Topic 1: [Enter topic name, e.g., "Networking Protocols"]

Topic 2: [Enter topic name, e.g., "Cybersecurity Threats"]


---

#### **Notes**

[Provide any additional notes, such as resources, reminders, or motivational messages.]

---