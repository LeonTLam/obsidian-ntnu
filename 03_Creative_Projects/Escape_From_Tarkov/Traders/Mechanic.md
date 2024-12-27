---
tags:
  - Trader
Trader:
  - "[[Mechanic]]"
Wares:
  - Weapons
  - Magazines
  - Ammo
  - Mods
  - Keycards
  - Special Equipment
  - Storage Containers
Buys:
  - Weapons
  - Ammo
  - Mods
  - Keycards
  - Barter Items
  - Special Equipment
Services:
  - Repairs
Currencies:
  - Euros (€)
  - Roubles (₽)
Quests: 
  - "[[Saving the Mole]]"
  - "[[Gunsmith - Part 1]]"
  - "[[Introduction]]"
  - "[[Gunsmith - Part 2]]"
  - "[[Gunsmith - Part 3]]"
  - "[[Gunsmith - Part 4]]"
  - "[[Gunsmith - Part 5]]"
  - "[[Bad Habit]]"
  - "[[Black Swan]]"
  - "[[Broadcast - Part 1]]"
  - "[[Capacity Check]]"
  - "[[Farming - Part 1]]"
  - "[[Farming - Part 2]]"
  - "[[Forklift Certified]]"
  - "[[Insider]]"
  - "[[Scout]]"
  - "[[Signal - Part 1]]"
  - "[[Signal - Part 2]]"
  - "[[A Shooter Born in Heaven]]"
  - "[[Back Door]]"
  - "[[Farming - Part 3]]"
  - "[[Farming - Part 4]]"
  - "[[Gunsmith - Part 6]]"
  - "[[Surplus Goods]]"
  - "[[Gunsmith - Part 7]]"
  - "[[Signal - Part 3]]"
  - "[[Signal - Part 4]]"
  - "[[Corporate Secrets]]"
  - "[[Gunsmith - Part 8]]"
  - "[[Gunsmith - Part 9]]"
  - "[[Gunsmith - Part 10]]"
  - "[[Chemistry Closet]]"
  - "[[Gunsmith - Part 11]]"
  - "[[Gunsmith - Part 12]]"
  - "[[Energy Crisis]]"
  - "[[Gunsmith - Part 13]]"
  - "[[Gunsmith - Part 14]]"
  - "[[Gunsmith - Part 15]]"
  - "[[Fertilizers]]"
  - "[[Gunsmith - Part 16]]"
  - "[[Gunsmith - Part 17]]"
  - "[[Gunsmith - Part 18]]"
  - "[[Import]]"
  - "[[Psycho Sniper]]"
  - "[[Gunsmith - Part 19]]"
  - "[[Gunsmith - Part 20]]"
  - "[[Gunsmith - Part 21]]"
  - "[[Gunsmith - Part 22]]"

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
