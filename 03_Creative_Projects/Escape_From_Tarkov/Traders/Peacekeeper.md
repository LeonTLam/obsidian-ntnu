---
tags:
  - Trader
Trader:
  - "[[Peacekeeper]]"
Wares:
  - "[[Weapons]]"
  - "[[Gear]]"
  - "[[Magazines]]"
  - "[[Ammo]]"
  - "[[Grenades]]"
  - "[[Mods]]"
  - "[[Storage Containers]]"
  - Dollars ($)
Buys:
  - "[[Armored Gear]]"
  - "[[Weapons]]"
  - "[[Ammo]]"
  - "[[Mods]]"
  - "[[Keycards]]"
  - "[[Barter Items]]"
  - "[[Info Items]]"
  - "[[Special Equipment]]"
Services:
  - None
Currencies:
  - Dollars ($)
Quests:
  - "[[Fishing Gear]]"
  - "[[Scrap Metal]]"
  - "[[Tigr Safari]]"
  - "[[Eagle Eye]]"
  - "[[Humanitarian Supplies]]"
  - "[[Cargo X - Part 1]]"
  - "[[Cargo X - Part 2]]"
  - "[[Cargo X - Part 3]]"
  - "[[Cargo X - Part 4]]"
  - "[[Insomnia]]"
  - "[[Spa Tour - Part 1]]"
  - "[[Spa Tour - Part 2]]"
  - "[[Spa Tour - Part 3]]"
  - "[[Spa Tour - Part 4]]"
  - "[[Spa Tour - Part 5]]"
  - "[[Spa Tour - Part 6]]"
  - "[[Spa Tour - Part 7]]"
  - "[[The Cult - Part 1]]"
  - "[[The Cult - Part 2]]"
  - "[[Classified Technologies]]"
  - "[[Revision - Lighthouse]]"
  - "[[Revision - Reserve]]"
  - "[[Wet Job - Part 1]]"
  - "[[Wet Job - Part 2]]"
  - "[[Wet Job - Part 3]]"
  - "[[Wet Job - Part 4]]"
  - "[[Wet Job - Part 5]]"
  - "[[Wet Job - Part 6]]"
  - "[[Overpopulation]]"
  - "[[Samples]]"
  - "[[TerraGroup Employee]]"
  - "[[Lend-Lease - Part 2]]"
  - "[[One Less Loose End (choice)]]"
  - "[[Peacekeeping Mission]]"
  - "[[The Guide]]"

inSelect: All
hideCompleted: false
inSearch: ""
Cover: "![[Peacekeeper_Portrait.webp]]"
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

| Loyalty Level 1                  | Loyalty Level 2 ---->            | Loyalty Level 3                  | Loyalty Level 4                  |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| ![[Peacekeeper1Stock.webp\|300]] | ![[Peacekeeper2Stock.webp\|300]] | ![[Peacekeeper3Stock.webp\|300]] | ![[Peacekeeper4Stock.webp\|300]] |
