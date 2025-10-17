---
excalidraw-border-color: transparent
excalidraw-default-mode: view
---
```dataviewjs
const parentFolder = dv.current().file.folder.replace(/\/[^/]*$/, '');
const pcFile = dv.pages(`"${parentFolder}"`).where(p => p.file.name.startsWith("PC -")).first();

const modifier = pcFile?.strength_modifier || 0;
const displayModifier = modifier >= 0 ? `+${modifier}` : modifier;
const color = pcFile?.ability_colors?.strength || "#228B22";

dv.paragraph(`
<div style="font-size: 130px; font-weight: bold; line-height: 0.9; padding: 0; margin: -20px 0px 0px 0px; text-align: centre;">
  <div style="color: ${color}; padding: 0; margin: 0;">${displayModifier}</div>
</div>
`)
```
