```dataview
table 
  format as "Typ",
  phase as "Phase",
  status as "Status",
  rating as "★"
from "MCU"
where type = "mcu"
sort timeline_year asc, release_year asc
```
