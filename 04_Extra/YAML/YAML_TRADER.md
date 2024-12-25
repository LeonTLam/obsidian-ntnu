---
tags:
  - Trader
Trader:
  - Prapor
  - Therapist
  - Fence
  - Skier
  - Peacekeeper
  - Mechanic
  - Ragman
  - Jaegar
  - Ref
Wares:
  - Gear
  - Magazines
  - Ammo
  - Grenades
  - Mods
  - Storage Containers
  - Maps
  - Keys
  - Anything
  - Euros (€)
  - Dollars ($)
  - Weapons
  - Keycards
  - Special Equipment
Buys:
  - Body Armor
  - Weapons
  - Grenades
  - Ammo
  - Mods
  - Meds
  - Provisions
  - Mechanical Keys
  - Barter Items
  - Everything
  - Gear
  - Stimulants
  - Armored Gear
  - Keycards
  - Info Items
  - Special Equipment
  - Paracord
  - Fabric
  - Backpacks
  - Tactical Rigs
Services:
  - Insurance
  - Repairs
  - After raid healing
  - Tactical clothing
Currencies:
  - Roubles (₽)
  - Euros (€)
  - Dollars ($)
  - GP coin
Quests:
---
```dataview
table file.link as "Title", 
      Item_name as "Item Name", 
      Description as "Description", 
      Category
from #Quest 
where exists(Item_name)
sort file.name asc

```

```dataview
table 
    Maps as "Map", 
    Trader as "Trader", 
    Desc as "Description", 
    Kappa as "Status (Completion)", 
    "Lvl. Req." as "Level Requirement"
from #Quest
where exists(Maps) and exists(Trader) and exists(Desc)
sort file.name asc

```



