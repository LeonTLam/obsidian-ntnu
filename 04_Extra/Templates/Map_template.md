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

# Map

Image of Map

## Spawns

IMAGE of SPAWNS

## Extractions

IMAGE of EXTRACTIONS

Conditions to Extractions

# Quests


## POIs


