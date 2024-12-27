---
tags:
  - Trader
Trader:
  - "[[Ragman]]"
Wares:
  - Tactical Clothing
  - Gear
Buys:
  - Gear
  - Backpacks
  - Storage Containers
  - Fabric
  - Paracord
Services:
  - Tactical clothing
Currencies:
  - Roubles (₽)
Quests: 
  - "[[A Fuel Matter]]"
  - "[[Big Sale]]"
  - "[[Database - Part 1]]"
  - "[[Database - Part 2]]"
  - "[[Dressed to Kill]]"
  - "[[Gratitude]]"
  - "[[Inventory Check]]"
  - "[[Make ULTRA Great Again]]"
  - "[[Only Business]]"
  - "[[The Blood of War - Part 1]]"
  - "[[Minibus]]"
  - "[[Charisma Brings Success]]"
  - "[[Sew it Good - Part 1]]"
  - "[[Sew it Good - Part 2]]"
  - "[[Sew it Good - Part 3]]"
  - "[[Sew it Good - Part 4]]"
  - "[[The Blood of War - Part 2]]"
  - "[[No Fuss Needed]]"
  - "[[The Key to Success]]"
  - "[[Living High is Not a Crime - Part 1]]"
  - "[[Hot Delivery]]"
  - "[[Scavenger]]"
  - "[[Living High is Not a Crime - Part 2]]"
  - "[[Sales Night]]"
  - "[[The Blood of War - Part 3]]"
  - "[[Supervisor]]"

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
