```dataview  
list
from "MCU"
where status != "completed"
where !startswith(file.name, "_MCU")
sort timeline_year asc
```
