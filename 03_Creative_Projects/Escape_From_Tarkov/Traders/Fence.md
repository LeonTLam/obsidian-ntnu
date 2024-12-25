---
tags:
  - Trader
Trader:
  - "[[Fence]]"
Wares:
  - Ammo
  - Dollars ($)
  - Gear
  - Keycards
Buys:
  - Armored Gear
  - Barter Items
  - Everything
  - Fabric
Services:
  - Repairs
Currencies:
  - Roubles (₽)
Quests:
  - "[[A Fuel Matter]]"
  - "[[A Healthy Alternative (choice)]]"
  - "[[A Shooter Born in Heaven]]"
  - "[[Acquaintance]]"
  - "[[All is Revealed]]"
  - "[[Ambulance]]"
  - "[[Anesthesia]]"
  - "[[Athlete]]"
  - "[[Back Door]]"
  - "[[Background Check]]"
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
