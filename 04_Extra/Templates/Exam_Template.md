<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the concept a Title");
	await tp.file.rename(tp.date.now(title);
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
await tp.file.move("/01_Current_Semester/" + course + "/Exams/" + title)

_%>


#### **Exam Details**

- **Title**: [Enter Exam Title]
- **Course**: <% course %>
- **Due Date**: [Enter Due Date]
- **Description**: [Provide a brief description of the exam, including its purpose, format, and any important details.]

---

#### **Progress with Tasks**

tasks
- [ ] Review notes from lectures
  due:: [Task-specific due date, if any]

- [ ] Practice past exams
  due:: [Task-specific due date, if any]

- [ ] Create a summary of key topics
  due:: [Task-specific due date, if any]


(Add more tasks as needed.)

---

#### **Topics**

Topic 1: [Enter topic name, e.g., "Networking Protocols"]

Topic 2: [Enter topic name, e.g., "Cybersecurity Threats"]

(Add more topics as needed.)

---

#### **Notes**

[Provide any additional notes, such as resources, reminders, or motivational messages.]

---