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
# Maps
```dataview
table 
    Duration as "Duration",
    Players as "PMCs",
    length(filter(from("03_Creative_Projects/Escape_From_Tarkov/Quests"), q => contains(q.Maps, this.Maps))) as "Total Quests"
from "03_Creative_Projects/Escape_From_Tarkov/Locations"
where Maps
sort file.name asc
```

```dataview
table 
    Duration as "Duration",
    Players as "PMCs",
    length(filter(from("03_Creative_Projects/Escape_From_Tarkov/Quests"), q => contains(q.Maps, this.file.name))) as "Total Quests"
from "03_Creative_Projects/Escape_From_Tarkov/Locations"
where Maps
sort file.name asc
```
# Traders
```dataview
table 
    Cover as "Cover", 
    Services as "Services", 
    Currencies as "Currencies", 
	length(Quests) as "Total Quests"
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
where Quests
sort file.name asc
```



