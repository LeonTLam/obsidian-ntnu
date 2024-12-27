---
tags:
  - Trader
Trader:
  - "[[Jaegar]]"
Wares:
  - "[[Weapons]]"
  - "[[Magazines]]"
  - "[[Ammo]]"
  - "[[Mods]]"
  - "[[Gear]]"
  - "[[Special Equipment]]"
  - "[[Storage Containers]]"
Buys:
  - "[[Tactical Rigs]]"
  - "[[Backpacks]]"
  - "[[Weapons]]"
  - "[[Mods]]"
  - "[[Meds]]"
  - "[[Provisions]]"
  - "[[Barter Items]]"
  - "[[Storage Containers]]"
  - "[[Secure Containers]]"
Services:
  - None
Currencies:
  - Roubles (₽)
Quests: 
  - "[[Acquaintance]]"
  - "[[Claustrophobia]]"
  - "[[Every Hunter Knows This]]"
  - "[[Rough Tarkov]]"
  - "[[The Huntsman Path - Controller]]"
  - "[[The Huntsman Path - Evil Watchman]]"
  - "[[The Huntsman Path - Forest Cleaning]]"
  - "[[The Huntsman Path - Justice]]"
  - "[[The Huntsman Path - Outcasts]]"
  - "[[The Huntsman Path - Secured Perimeter]]"
  - "[[The Huntsman Path - Trophy]]"
  - "[[The Survivalist Path - Combat Medic]]"
  - "[[The Survivalist Path - Eagle-Owl]]"
  - "[[The Survivalist Path - Junkie]]"
  - "[[The Survivalist Path - Thrifty]]"
  - "[[The Survivalist Path - Tough Guy]]"
  - "[[The Survivalist Path - Unprotected but Dangerous]]"
  - "[[The Survivalist Path - Wounded Beast]]"
  - "[[The Survivalist Path - Zhivchik]]"
  - "[[The Tarkov Shooter - Part 1]]"
  - "[[The Tarkov Shooter - Part 2]]"
  - "[[The Tarkov Shooter - Part 3]]"
  - "[[The Tarkov Shooter - Part 4]]"
  - "[[The Tarkov Shooter - Part 5]]"
  - "[[The Tarkov Shooter - Part 6]]"
  - "[[The Tarkov Shooter - Part 7]]"
  - "[[The Tarkov Shooter - Part 8]]"
  - "[[The Delicious Sausage]]"
  - "[[The Huntsman Path - Factory Chief]]"
  - "[[The Huntsman Path - Woods Keeper]]"
  - "[[Dragnet]]"
  - "[[Courtesy Visit]]"
  - "[[Pest Control]]"
  - "[[Reserve]]"
  - "[[Shady Business]]"
  - "[[The Hermit]]"
  - "[[The Huntsman Path - Eraser - Part 1]]"
  - "[[The Huntsman Path - Eraser - Part 2]]"
  - "[[The Huntsman Path - Sadist (choice)]]"
  - "[[Ambulance]]"
  - "[[Fishing Place]]"
  - "[[Nostalgia]]"
  - "[[The Huntsman Path - Sellout]]"
  - "[[Hunting Trip]]"
  - "[[Stray Dogs]]"
inSearch: ""
inSelect:
  - All
hideCompleted: false
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
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where (this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect) AND (Trader = this.Trader) AND ((this.hideCompleted = false) OR (this.hideCompleted = true AND !contains(Status, "Completed"))) and (this.inSearch = "" or contains(lower(file.name), lower(this.inSearch)))
sort number(LvlReq) asc
```

# Items for Sale

| Loyalty Level 1 | Loyalty Level 2 ----> | Loyalty Level 3 | Loyalty Level 4 |
| --------------- | --------------------- | --------------- | --------------- |
| ![[a\|300]]     | ![[a\|300]]           | ![[a\|300]]     | ![[a\|300]]     |
