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

| Tech -> First -> Second    | Exf.                                                                                                                               |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| ![[Labs_Tech_e.png\|500]]  | North: **Main Elevator<br><br>East: **Sewage Conduit**<br><br>South: **Medical Block Entrance**<br><br>West: **Ventilation Shaft** |
| ![[Laps_First_e.png\|500]] | North West: **Parking Gate**<br><br>South West: **Transit [[Streets of Tarkov]]**<br><br>East: **Hangar Gate**                     |
| ![[Labs_Sec_e.png\|500]]   | South: **Cargo Elevator**                                                                                                          |

| Name           | Availability | Single-use | Requirements |
| -------------- | ------------ | ---------- | ------------ |
| Cargo Elevator | ✅            | ✅          |              |
|                |              |            |              |
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



