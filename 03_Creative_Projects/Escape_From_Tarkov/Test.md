


```dataview
table 
    Cover as "Cover", 
    Trader as "Trader", 
    Services as "Services", 
    Currencies as "Currencies", 
    length(filter(Quests, q => q.Trader = this.Trader and q.Status = "- ✅ Completed")) 
    as "Completed Quests", 
    length(filter(Quests, q => q.Trader = this.Trader)) as "Total Quests", 
    (length(filter(Quests, q => q.Trader = this.Trader and q.Status = "Completed")) + "/" + length(filter(Quests, q => q.Trader = this.Trader))) as "Quest Progress",
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
sort file.name asc

```




