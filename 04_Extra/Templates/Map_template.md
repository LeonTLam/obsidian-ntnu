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

const parentFolder = "03_Creative_Projects/Escape_From_Tarkov/Locations/";

// Output the selected course or use it in your script
await tp.file.move(parentFolder + title)
_%>
`BUTTON[return]`
# Map

Image of Map

## Spawns

IMAGE of SPAWNS

## Extractions

IMAGE of EXTRACTIONS

Conditions to Extractions

## POIs

Point of Interest
# Quests

```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where Maps = this.Maps
sort this.LvlReq asc
```



