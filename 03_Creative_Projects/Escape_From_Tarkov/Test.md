```meta-bind
bind: QuestsCompletedCounter
eval: length(filter(from("Quests"), q => q.file.frontmatter.Status = "✅ Completed"))
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




