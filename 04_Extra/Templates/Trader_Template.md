---
tags:
  - Trader
Trader:
Wares:
Buys:
Services:
Currencies:
Quests:
---
<%*
const hasTitle = !tp.file.title.startsWith("Untitl");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the concept a Title");
	await tp.file.rename(title);
} else {
	title = tp.file.title;
}

const parentFolder = "03_Creative_Projects/Escape_From_Tarkov/Traders/";

// Output the selected course or use it in your script
await tp.file.move(parentFolder + title)
_%>

# Quests

```meta-bind-embed
[[META_BUTTONS]]
```
`BUTTON[return]` 
```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Status as "Status (Completion)", 
    LvlReq as "Level Requirement"
from "03_Creative_Projects/Escape_From_Tarkov/Quests"
where Trader = this.Trader
sort this.LvlReq asc
```

# Items for Sale

| Loyalty Level 1                  | Loyalty Level 2 ---->            | Loyalty Level 3                  | Loyalty Level 4                  |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
|  |  |  |  |
