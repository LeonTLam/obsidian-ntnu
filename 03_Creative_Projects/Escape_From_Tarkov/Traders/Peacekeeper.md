---
tags:
  - Trader
Trader:
  - "[[Peacekeeper]]"
Wares: 
Buys: 
Services: 
Currencies: 
Quests:
---
# Quests

```dataview
table 
    Maps as "Map", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where Trader = this.Trader
sort this.LvlReq asc
```
