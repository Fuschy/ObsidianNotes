
```dataview  
table  
length(rows) as "Gesamt",  
length(filter(rows, (r) => r.status = "completed")) as "Gesehen",  
round(  
length(filter(rows, (r) => r.status = "completed"))  
/ length(rows) * 100  
,1) as "Fortschritt %"  
from #MCU
where file.name != "TEMPLATE_MCU"
```
