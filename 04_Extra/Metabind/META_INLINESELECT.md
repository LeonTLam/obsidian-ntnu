---
inSelect: Ground Zero
---


```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where inSelect != null AND (contains(inSelect, this.
sort this.LvlReq asc
```