---
tags:
  - Trader
Trader:
  - "[[Skier]]"
Wares:
  - "[[Weapons]]"
  - "[[Magazines]]"
  - "[[Ammo]]"
  - "[[Mods]]"
  - "[[Storage Containers]]"
  - Euros (€)
Buys:
  - "[[Gear]]"
  - "[[Weapons]]"
  - "[[Grenades]]"
  - "[[Ammo]]"
  - "[[Mods]]"
  - "[[Stimulants]]"
  - "[[Barter Items]]"
Services:
  - Repairs
Currencies:
  - Roubles (₽)
  - Dollars ($)
  - Euros (€)
Quests:
  - "[[Burning Rubber]]"
  - "[[Supplier]]"
  - "[[The Extortionist]]"
  - "[[Golden Swag]]"
  - "[[Stirrup]]"
  - "[[What’s on the Flash Drive?]]"
  - "[[Friend From the West - Part 1]]"
  - "[[Friend From the West - Part 2]]"
  - "[[Chemical - Part 1]]"
  - "[[Chemical - Part 2]]"
  - "[[Chemical - Part 3]]"
  - "[[Chemical - Part 4 (choice)]]"
  - "[[Exit Here]]"
  - "[[The Walls Have Eyes]]"
  - "[[Kind of Sabotage (choice)]]"
  - "[[Safe Corridor]]"
  - "[[Setup]]"
  - "[[Long Road]]"
  - "[[Rigged Game]]"
  - "[[Vitamins - Part 1]]"
  - "[[Vitamins - Part 2]]"
  - "[[Informed Means Armed]]"
  - "[[Lend-Lease - Part 1]]"
  - "[[Chumming]]"
  - "[[Missing Cargo]]"
  - "[[Flint]]"
inSearch: ""
inSelect:
  - All
hideCompleted: false
Cover: "![[Skier_Portrait.webp]]"
---
# Quests
```meta-bind-embed
[[META_BUTTONS]]
```
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
FLATTEN row["Trader"] as Trader
FLATTEN row["Maps"] as Maps
FLATTEN row["Status"] as Status
FLATTEN row["LvlReq"] as LvlReq
sort number(LvlReq) asc
```

# Items for Sale

| Loyalty Level 1            | Loyalty Level 2 ---->      | Loyalty Level 3            | Loyalty Level 4            |
| -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| ![[Skier1Stock.webp\|300]] | ![[Skier2Stock.webp\|300]] | ![[Skier3Stock.webp\|300]] | ![[Skier4Stock.webp\|300]] |
