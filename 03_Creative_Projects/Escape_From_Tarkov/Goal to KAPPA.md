---
inSelect: All
inSearch: ""
hideCompleted: false
inSelect2: All
---
This document serves as a comprehensive guide for **Escape from Tarkov**, specifically tailored to help you unlock the coveted **Secure Container [[Kappa]]**. Inside, you'll find essential details about the game's [[Goal to KAPPA#Maps|maps]], key [[Goal to KAPPA#Traders|traders]], and crucial items required to complete the challenging [[Goal to KAPPA#Quests|quests]] leading to Kappa. Use this guide to streamline your journey and maximize your efficiency in achieving this ultimate milestone.
```dataviewjs
// CONFIGURATION
const sourceFolder = "03_Creative_Projects/Escape_From_Tarkov/Quests"; // Adjust folder path
const yamlField = "Status"; // YAML field to group by

// Retrieve all pages and group by status
const all = dv.pages(`"${sourceFolder}"`)
    .groupBy(p => p.file.frontmatter[yamlField]) // Group by Status (e.g., "✅ Completed")
    .values // Convert Dataview groups to an array
    .map(p => `${p.key || "No Status"} ${"▬".repeat(p.rows.length)} ${p.rows.length}`) // Map to bar chart format
    .reverse(); // Reverse to show completed first (optional)

// Calculate Total Quests
const total = dv.pages(`"${sourceFolder}"`).length || 0;
const totalBar = `⭐ Total Quests ${"▬".repeat(total)} ${total}`;

// Append Total Quests to the results
all.push(totalBar);

// Display results
dv.header(3, `Quest Progress for KAPPA`);
dv.list(all);

```
# Quests

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 

| **Search by Name**                              | **Filter by Map**                                                                                                                                                                                                                                            | **Filter by Trader**                                                                                                                                                                               | **Hide Completed Quests**     |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| `INPUT[text(placeholder(Quest Name)):inSearch]` | `INPUT[inlineSelect(option(The Lab), option(Ground Zero), option(Streets of Tarkov), option(Interchange), option(Customs), option(Factory), option(Woods), option(Lighthouse), option(Reserve), option(Shoreline), option(Anywhere), option(All)):inSelect]` | `INPUT[inlineSelect(option(Fence), option(Jaegar), option(Mechanic), option(Peacekeeper), option(Prapor), option(Ragman), option(Ref), option(Skier), option(Therapist),  option(All)):inSelect2]` | `INPUT[toggle:hideCompleted]` |

```dataview
table

    Maps as "Map",

    Trader as "Trader",

    Status as "Status (Completion)",

    LvlReq as "Level Requirement"

from "03_Creative_Projects/Escape_From_Tarkov/Quests"

where

    ((this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect))

    AND ((this.hideCompleted = false) OR (this.hideCompleted = true AND !contains(Status, "Completed")))

    AND ((this.inSelect2 = "" or this.inSelect2 = "All") OR contains(Trader.file.name, this.inSelect2))

    AND (this.inSearch = "" or contains(lower(file.name), lower(this.inSearch)))

FLATTEN row["Trader"] as Trader

FLATTEN row["Maps"] as Maps

FLATTEN row["Status"] as Status

FLATTEN row["LvlReq"] as LvlReq

sort number(LvlReq) asc
```

# Maps
```dataview
table WITHOUT ID
	Map as "Locations",
    Duration as "Duration", 
    Players as "PMCs"
from "03_Creative_Projects/Escape_From_Tarkov/Locations"
FLATTEN row["Maps"] as Map
sort file.name asc
```
# Traders
```dataview
table WITHOUT ID
	Trader as "Traders",
    Cover as "Cover", 
    Services as "Services", 
    Currencies as "Currencies", 
	length(Quests) as "Total Quests"
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
where Quests
FLATTEN row["Trader"] as Trader
sort file.name asc
```



