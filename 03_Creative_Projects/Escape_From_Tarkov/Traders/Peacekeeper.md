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
inSelect: All
hideCompleted: false
---
# Quests

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 

**Filter by Map**
`INPUT[inlineSelect(option(The Lab), option(Ground Zero), option(Streets of Tarkov), option(Interchange), option(Customs), option(Factory), option(Woods), option(Lighthouse), option(Reserve), option(Shoreline), option(Anywhere), option(All)):inSelect]`

**Hide Completed Quests**
`INPUT[toggle:hideCompleted]`
```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where (this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect) AND (Trader = this.Trader) AND (this.hideCompleted = false AND Status != "✅ Completed")
sort number(LvlReq) asc
```
# Items for Sale

| Loyalty Level 1                  | Loyalty Level 2 ---->            | Loyalty Level 3                  | Loyalty Level 4                  |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| ![[Peacekeeper1Stock.webp\|300]] | ![[Peacekeeper2Stock.webp\|300]] | ![[Peacekeeper3Stock.webp\|300]] | ![[Peacekeeper4Stock.webp\|300]] |
