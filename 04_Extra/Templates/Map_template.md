---
tags:
  - Map
Maps: []
Bosses: 
Quests: 
Duration: 
Players: 
Enemies: 
inSelect:
  - All
inSearch: ""
hideCompleted: false
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

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 

**Search by Name**
`INPUT[text:inSearch]`

**Filter by Trader**
`INPUT[inlineSelect(option(Prapor), option(Therapist), option(Fence), option(Skier), option(Peacekeeper), option(Mechanic), option(Ragman), option(Jaegar), option(All)):inSelect]`

**Hide Completed Quests**
`INPUT[toggle:hideCompleted]`
```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where (this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect) AND (Maps = this.Maps) AND ((this.hideCompleted = false) OR (this.hideCompleted = true AND !contains(Status, "Completed"))) and (this.inSearch = "" or contains(lower(file.name), lower(this.inSearch)))
sort number(LvlReq) asc
```
