---
inSelect: Ground Zero
---
`INPUT[inlineSelect(option(The Lab), option(Peacekeeper), option(Ground Zero)):inSelect]`

```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where  = this.Trader
sort this.LvlReq asc
```