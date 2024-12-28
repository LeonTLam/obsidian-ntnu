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
where (this.inSelect = "" or this.inSelect = "All") OR contains(Maps.file.name, this.inSelect) AND ((this.hideCompleted = false) OR (this.hideCompleted = true AND !contains(Status, "Completed"))) and (this.inSearch = "" or contains(lower(file.name), lower(this.inSearch)))
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



