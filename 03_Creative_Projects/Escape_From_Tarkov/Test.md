


```dataview
table 
    Cover as "Cover", 
    Trader as "Trader", 
    Services as "Services", 
    Currencies as "Currencies", 
    length(Quests) as "Q"
from "03_Creative_Projects/Escape_From_Tarkov/Traders"
where Quests
sort file.name asc

```




