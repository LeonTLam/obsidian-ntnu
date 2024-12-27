```dataviewjs
// CONFIGURATION
const sourceFolder = "Quests"; // Folder where quests are located
const statusField = "Status"; // YAML field to check

// Retrieve pages and group by status
const questData = dv.pages(`"${sourceFolder}"`)
    .groupBy(p => p.file.frontmatter[statusField] || "No Status");

// Debugging Logs
console.log("Quest Data (Raw):", questData);

// Process grouped data
const questCounts = questData.map(p => `${p.key},${p.rows.length}`);
console.log("Quest Counts (Processed):", questCounts);

// Extract Completed Quests
const completed = parseInt(questCounts.find(d => d.startsWith("✅ Completed"))?.split(",")[1] || 0);
const total = dv.pages(`"${sourceFolder}"`).length;
const remaining = total - completed;

// Debug Completed/Remaining Quests
console.log("Completed Quests:", completed);
console.log("Remaining Quests:", remaining);

// Build TinyChart
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




