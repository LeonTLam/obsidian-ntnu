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

![[ShorelineSpawns.png]]

## Extractions

![[ShorelineExtract.png]]

| Extraction/Transit Name   | Faction     | Always Available | Single-Use | Requirements                                         | Notes                                       |
| ------------------------- | ----------- | ---------------- | ---------- | ---------------------------------------------------- | ------------------------------------------- |
| Admin Basement            | Scav        | ✅                | ❌          | None                                                 |                                             |
| Climber's Trail           | PMC         | ✅                | ❌          | Red Rebel ice pick, Paracord, No armor vest equipped |                                             |
| East Wing Gym Entrance    | Scav        | ✅                | ❌          | None                                                 |                                             |
| Lighthouse                | Scav        | ✅                | ❌          | None                                                 |                                             |
| Old Bunker                | Scav        | ✅                | ❌          | None                                                 |                                             |
| Path to Lighthouse        | PMC         | ✅                | ❌          | None                                                 |                                             |
| Pier Boat                 | PMC         | ✅                | ❌          | Green flare = Open                                   |                                             |
| Railway Bridge            | PMC         | ✅                | ❌          | None                                                 |                                             |
| Road to Customs           | SCAV<br>PMC | ✅                | ❌          | None                                                 |                                             |
| Road to North V-Ex        | PMC         | ✅                | ✅          | Payment per player                                   | Max 5 players; fee influenced by Scav karma |
| Ruined Road               | Scav        | ✅                | ❌          | None                                                 |                                             |
| Smuggler's Path (Co-op)   | SCAV<br>PMC | ✅                | ❌          | Scav and PMC present                                 |                                             |
| Tunnel                    | PMC         | ✅                | ❌          | None                                                 |                                             |
| Transit to [[Lighthouse]] | SCAV<br>PMC | ✅                | ❌          | Accessible 1 minute after raid start                 | In front of Path to Lighthouse extraction   |

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
