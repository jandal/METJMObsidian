---
excalidraw-border-color: transparent
excalidraw-default-mode: view
---
```dataviewjs
const parentFolder = dv.current().file.folder.replace(/\/[^/]*$/, '');
const pcFile = dv.pages(`"${parentFolder}"`).where(p => p.file.name.startsWith("PC -")).first();
const color = pcFile?.primary_color || "#06A77D";

const skillValue = pcFile?.skill_history || 0;
const displayValue = skillValue >= 0 ? `+${skillValue}` : skillValue;

dv.paragraph(`
<div style="font-size: 32px; font-weight: bold; color: ${color}; text-align: center;">
  ${displayValue}
</div>
`)
```
