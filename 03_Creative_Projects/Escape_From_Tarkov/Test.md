```Dataview
table 
    file.link as "Trade Name", 
    Trader as "Trader", 
    Items as "Items Traded", 
    Description as "Description"
from "Traders"
where contains(tags, "#Trader")
sort file.name asc
```

