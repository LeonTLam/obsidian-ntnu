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
inSelect: Ground
---
# Quests

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 

**Filter by 
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


`INPUT[inlineSelect(option(Not Started), option(Peace), option(Ground)):inSelect]`

```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where contains(Trader.file.name, this.inSelect) or contains(Maps.file.name, this.inSelect)
sort this.LvlReq asc
```

# Items for Sale

| Loyalty Level 1                  | Loyalty Level 2 ---->            | Loyalty Level 3                  | Loyalty Level 4                  |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| ![[Peacekeeper1Stock.webp\|300]] | ![[Peacekeeper2Stock.webp\|300]] | ![[Peacekeeper3Stock.webp\|300]] | ![[Peacekeeper4Stock.webp\|300]] |
