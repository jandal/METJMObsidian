---
excalidraw-border-color: transparent
excalidraw-default-mode: view
---
```dataviewjs
const parentFolder = dv.current().file.folder.replace(/\/[^/]*$/, '');
const pcFile = dv.pages(`"${parentFolder}"`).where(p => p.file.name.startsWith("PC -")).first();

const color = pcFile?.primary_color || "#06A77D";

dv.paragraph(`
<div style="font-size: 40px; font-weight: bold; line-height: 0.9; padding: 0; margin: -20px 0px 0px 0px; text-align: centre;">
  <div style="color: ${color}; padding: 0; margin: 0;">${pcFile?.level || "?"}</div>
</div>
`)
```
