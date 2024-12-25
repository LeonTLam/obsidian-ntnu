---
tags:
  - Trader
Trader:
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
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where Trader = this.Trader
sort this.LvlReq asc
```
