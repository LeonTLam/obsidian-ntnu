---
tags:
  - Quest
Kappa: true
Maps: 
Trader: 
Status: 🛑 Not Started
LvlReq: 
Item: 
Enemies: 
Bosses: 
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

const parentFolder = "03_Creative_Projects/Escape_From_Tarkov/Quests/";

// Output the selected course or use it in your script
await tp.file.move(parentFolder + title)
_%>
# Quest
```meta-bind-embed
[[META_BUTTONS]]
```
```meta-bind-embed
[[META_QUEST]]
```
## Task

* Task1
* Task2

## Guide
`= "[" + this.file.name + "](https://escapefromtarkov.fandom.com/wiki/" + this.file.name + ")"`
## Location

