---
tags:
  - Trader
Trader:
  - "[[Skier]]"
Wares:
  - Weapons
  - Magazines
  - Ammo
  - Mods
  - Storage Containers
  - Euros (€)
Buys:
  - Gear
  - Weapons
  - Grenades
  - Ammo
  - Mods
  - Stimulants
  - Barter Items
Services:
  - Repairs
Currencies:
  - Roubles (₽)
  - Dollars ($)
  - Euros (€)
Quests:
---
# Quests

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 

**Search by Name**
`INPUT[text:inSearch]`

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
where (this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect) AND (Trader = this.Trader) AND ((this.hideCompleted = false) OR (this.hideCompleted = true AND !contains(Status, "Completed"))) and (this.inSearch = "" or contains(lower(file.name), lower(this.inSearch)))
sort number(LvlReq) asc
```

# Items for Sale

| Loyalty Level 1                  | Loyalty Level 2 ---->            | Loyalty Level 3                  | Loyalty Level 4                  |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
|  |  |  |  |
