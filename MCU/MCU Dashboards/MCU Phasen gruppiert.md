```dataview
table 
  timeline_year as "Timeline",
  format as "Typ",
  status as "Status",
  rating as "★"
from "MCU"
where type = "mcu"
group by phase
sort phase asc, timeline_year asc
```
