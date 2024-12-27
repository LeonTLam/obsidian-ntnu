


```dataview
table 
    Cover as "Cover", 
    Trader as "Trader", 
    Services as "Services", 
    Currencies as "Currencies", 
    length(Quests) as "Total Quests",
    length(filter(Quests, q => link(q).Status = "✅ Completed")) as "Completed"
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
where Quests
sort file.name asc
```




