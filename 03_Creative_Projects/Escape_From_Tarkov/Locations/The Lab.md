---
tags:
  - Map
Maps:
  - "[[The Lab]]"
Bosses: 
Quests: 
Duration:
  - 35 Min
Players:
  - 8-10
Enemies:
  - Scav Raiders
---

# Map

| Technical Level         | First Level              | Second Level           |
| ----------------------- | ------------------------ | ---------------------- |
| ![[Labs_Tech.png\|300]] | ![[Labs_First.png\|300]] | ![[Labs_Sec.png\|300]] |
| ![[Labs_First.png]]     |                          |                        |
| ![[Labs_Sec.png]]       |                          |                        |

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
where Trader = this.Maps
sort this.LvlReq asc
```



