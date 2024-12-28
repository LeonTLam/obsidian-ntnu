---
tags:
  - Trader
Trader:
  - "[[Therapist]]"
Wares:
  - "[[Meds]]"
  - "[[Provisions]]"
  - "[[Keys]]"
  - "[[Storage Containers]]"
  - Maps
Buys:
  - "[[Meds]]"
  - "[[Provisions]]"
  - "[[Keys]]"
  - "[[Barter Items]]"
  - "[[Storage Containers]]"
  - Maps
Services:
  - Insurance
  - After raid healing
Currencies:
  - Roubles (₽)
  - Euros (€)
Quests: 
  - "[[First in Line]]"
  - "[[Shortage]]"
  - "[[Sanitary Standards - Part 1]]"
  - "[[Operation Aquarius - Part 1]]"
  - "[[Operation Aquarius - Part 2]]"
  - "[[Painkiller]]"
  - "[[Sanitary Standards - Part 2]]"
  - "[[Car Repair]]"
  - "[[General Wares]]"
  - "[[Pharmacist]]"
  - "[[Postman Pat - Part 2]]"
  - "[[Out of Curiosity (choice)]]"
  - "[[All is Revealed]]"
  - "[[Supply Plans (choice)]]"
  - "[[A Healthy Alternative (choice)]]"
  - "[[Disease History]]"
  - "[[Seaside Vacation]]"
  - "[[Health Care Privacy - Part 1]]"
  - "[[Health Care Privacy - Part 2]]"
  - "[[Health Care Privacy - Part 3]]"
  - "[[Health Care Privacy - Part 4]]"
  - "[[Health Care Privacy - Part 5]]"
  - "[[Health Care Privacy - Part 6]]"
  - "[[Colleagues - Part 1]]"
  - "[[Colleagues - Part 2]]"
  - "[[Colleagues - Part 3 (choice)]]"
  - "[[Drug Trafficking]]"
  - "[[Lost Contact]]"
  - "[[Athlete]]"
  - "[[Decontamination Service]]"
  - "[[Private Clinic]]"
  - "[[Crisis]]"

inSearch: ""
inSelect:
  - All
hideCompleted: false
Cover: "![[Therapist_Portrait.webp]]"
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
FLATTEN row["Trader"] as Trader
FLATTEN row["Maps"] as Maps
FLATTEN row["Status"] as Status
FLATTEN row["LvlReq"] as LvlReq
sort number(LvlReq) asc
```

# Items for Sale

| Loyalty Level 1 | Loyalty Level 2 ----> | Loyalty Level 3 | Loyalty Level 4 |
| --------------- | --------------------- | --------------- | --------------- |
| ![[a\|300]]     | ![[a\|300]]           | ![[a\|300]]     | ![[a\|300]]     |
