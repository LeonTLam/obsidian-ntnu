---
tags:
  - Map
Maps:
  - "[[Shoreline]]"
Bosses:
  - "[[Sanitar]]"
  - "[[Big Pipe]]"
  - "[[Bird Eye]]"
Duration:
  - 45 Min
Players:
  - 10-14
Enemies:
  - Cultists
  - Scavs
inSelect:
  - All
inSearch: ""
hideCompleted: false
---
# Map

![[Shoreline3d.webp]]
## Spawns

![[Pasted image 20241230143840.png]]

## Extractions

IMAGE of EXTRACTIONS

Conditions to Extractions

## POIs

Point of Interest
# Quests
```meta-bind-embed
[[META_BUTTONS]]
```
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
