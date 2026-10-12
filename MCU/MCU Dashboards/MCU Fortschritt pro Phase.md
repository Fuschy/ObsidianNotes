```dataviewjs
const pages = dv.pages('"MCU"').where(p => p.type == "mcu");

const phases = [...new Set(pages.map(p => p.phase))].sort((a,b)=>a-b);

for (let phase of phases) {
  const phasePages = pages.where(p => p.phase == phase);
  const total = phasePages.length;
  const completed = phasePages.where(p => p.status == "completed").length;
  const percent = total > 0 ? ((completed / total) * 100).toFixed(0) : 0;

  dv.header(3, `Phase ${phase} – ${percent}%`);

  dv.el("progress", "", {
    value: completed,
    max: total
  });

  dv.paragraph(`${completed} / ${total} abgeschlossen`);
}
```
