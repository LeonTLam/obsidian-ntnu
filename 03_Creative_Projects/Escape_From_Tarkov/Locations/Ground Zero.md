---
tags:
  - Map
Maps:
  - "[[Ground Zero]]"
Bosses:
  - "[[Kollontay]]"
Quests:
  - "[[Burning Rubber]]"
Duration:
  - 35 Min
Players:
  - 9-10
  - 9-12
Enemies:
  - Scavs
  - Cultists
---

# Map

![[gzero.png]]

# Spawns

![[gzero_s.png]]

# Extractions

![[gzero_e.png]]

Conditions to Extractions

# POIs

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
where Trader = this.Maps
sort this.LvlReq asc
```



