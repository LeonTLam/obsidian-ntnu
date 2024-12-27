---
tags:
  - Map
Maps:
  - "[[Ground Zero]]"
Bosses:
  - "[[Kollontay]]"
Duration:
  - 35 Min
Players:
  - 9-10
  - 9-12
Enemies:
  - Scavs
  - Cultists
inSearch: ""
inSelect: All
hideCompleted: false
---
# Map

![[gzero.png]]

# Spawns

![[gzero_s.png]]

# Extractions

![[gzero_e.png]]

### Extractions

| Name                             | Faction     | Availability | Single-Use | Requirements                                                                  |
| -------------------------------- | ----------- | ------------ | ---------- | ----------------------------------------------------------------------------- |
| **Emercom Checkpoint**           | PMC<br>SCAV | ✅            | ❌          | None                                                                          |
| **Mira Ave**                     | PMC         | ✅            | ❌          | Shoot a green flare into the sky while inside the signal flare area.          |
| **Nakatani Basement Stairs**     | PMC<br>SCAV | ✅            | ❌          | None                                                                          |
| **Police Cordon V-Ex**           | PMC         | ✅            | ✅          | Maximum of 4 players; fee amount influenced by Scav karma.                    |
| **Scav Checkpoint (Co-op)**      | PMC<br>SCAV | ✅            | ❌          | Requires both Scav and PMC cooperation.<br>                                   |
| Transit to [[Streets of Tarkov]] | PMC<br>SCAV | ✅            | ❌          | Available 1 minute after raid start; located next to the Mira Ave extraction. |

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
# POIs

Point of Interest


