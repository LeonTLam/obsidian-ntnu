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
    Kappa as "Status", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Quests/"
where contains(tags, "#Quest")
sort file.name asc
```
