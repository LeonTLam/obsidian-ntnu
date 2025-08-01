---
tags:
  - Map
Maps:
  - "[[The Lab]]"
Duration:
  - 35 Min
Players:
  - 8-10
Enemies:
  - Scav Raiders
hideCompleted: false
inSelect: All
inSearch: ""
---
# Map

| Cellar -> First Floor -> Second Floor |
| ------------------------------------- |
| ![[Labs_Tech.png]]                    |
| ![[Labs_First.png]]                   |
| ![[Labs_Sec.png]]                     |

# Spawns

| Tech -> First -> Second |
| ----------------------- |
| ![[Labs_Tech_s.png]]    |
| ![[Labs_First_s.png]]   |
| ![[Labs_Sec_s.png]]     |
# Extractions

| Tech -> First -> Second    | Exf.                                                                                                                                 |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| ![[Labs_Tech_e.png\|500]]  | North: **Main Elevator**<br><br>East: **Sewage Conduit**<br><br>South: **Medical Block Entrance**<br><br>West: **Ventilation Shaft** |
| ![[Laps_First_e.png\|500]] | North West: **Parking Gate**<br><br>South West: **Transit [[Streets of Tarkov]]**<br><br>East: **Hangar Gate**                       |
| ![[Labs_Sec_e.png\|500]]   | South: **Cargo Elevator**                                                                                                            |

| **Tech Floor**                    | Availability     | Single-use | Requirements                           |
| --------------------------------- | ---------------- | ---------- | -------------------------------------- |
| **Main Elevator**                 | ✅                | ❌          | Restore power in basement, opposite R4 |
| **Sewage Conduit**                | ✅                | ❌          | Sink water level                       |
| **Medical Block Entrance**        | ✅                | ❌          | Power in basement G6                   |
| **Ventilation Shaft**             | ✅                | ❌          | No **[[Backpack]]**                    |
|                                   | **First Floor**  |            |                                        |
| **Parking Gate**                  | ❌                | ❌          | Open gate in Y21                       |
| **Transit [[Streets of Tarkov]]** | ✅                | ❌          | Avail. 1 min after raid start          |
| **Hangar Gate**                   | ❌                | ❌          | Open gate in B24                       |
|                                   | **Second Floor** |            |                                        |
| **Cargo Elevator**                | ✅                | ✅          | Power in basement G1                   |
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

## POIs

Point of Interest

