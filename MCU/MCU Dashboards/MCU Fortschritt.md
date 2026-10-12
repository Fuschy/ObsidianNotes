```dataviewjs
const pages = dv.pages('"MCU"').where(p => p.type == "mcu");

const total = pages.length;
const completed = pages.where(p => p.status == "completed").length;
const watching = pages.where(p => p.status == "watching").length;

const percent = total > 0 ? ((completed / total) * 100).toFixed(1) : 0;

dv.paragraph(`**Gesamt:** ${total}`);
dv.paragraph(`**Gesehen:** ${completed}`);
dv.paragraph(`**Aktiv:** ${watching}`);
dv.paragraph(`**Fortschritt:** ${percent}%`);

dv.el("progress", "", {
  value: completed,
  max: total
});
```
