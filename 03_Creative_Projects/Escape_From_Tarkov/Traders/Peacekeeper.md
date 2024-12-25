---
tags:
  - Trader
Trader:
  - "[[Peacekeeper]]"
Wares:
  - Weapons
  - Gear
  - Magazines
  - Ammo
  - Grenades
  - Mods
  - Storage Containers
  - Dollars ($)
Buys:
  - Armored Gear
  - Weapons
  - Ammo
  - Mods
  - Keycards
  - Barter Items
  - Info Items
  - Special Equipment
Services:
  - None
Currencies:
  - Dollars ($)
Quests:
  - "[[TerraGroup Employee]]"
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
