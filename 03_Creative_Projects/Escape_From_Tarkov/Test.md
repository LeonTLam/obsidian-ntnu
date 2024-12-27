```dataviewjs
// CONFIGURATION
const sourceFolder = "Quests"; // Folder where quests are located
const statusField = "Status"; // YAML field to check

// Retrieve pages and group by status
const questData = dv.pages(`"${sourceFolder}"`)
    .groupBy(p => p.file.frontmatter[statusField])
    .map(p => `${p.key || "No Status"},${p.rows.length}`);

// Add completed vs remaining for the chart
const completed = questData.find(d => d.startsWith("✅ Completed"))?.split(",")[1] || 0;
const total = dv.pages(`"${sourceFolder}"`).length;
const remaining = total - completed;

// Build TinyChart with completed and remaining quests
dv.header(3, `Quests Progress in "${sourceFolder}"`);
dv.span([
    "~~~tinychart",
    "type: pie",
    "data:",
    "  labels: [Completed, Remaining]",
    `  datasets: [{ data: [${completed}, ${remaining}], backgroundColor: ['#4caf50', '#f44336'] }]`,
    "options:",
    "  responsive: true",
    "~~~"
].join("\n"));

```
```dataview
table 
    Cover as "Cover", 
    Trader as "Trader", 
    Services as "Services", 
    Currencies as "Currencies", 
	length(Quests) as "Total Quests"
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
where Quests
sort file.name asc

```




