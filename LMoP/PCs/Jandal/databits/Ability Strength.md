---
excalidraw-font: Cascadia
excalidraw-border-color: transparent
excalidraw-css: |-
  body {
    background: transparent !important;
    padding: 0 !important;
    margin: 0 !important;
  }
  p {
    margin: 0 !important;
    padding: 0 !important;
  }
---
```dataviewjs
const parentFolder = dv.current().file.folder.replace(/\/[^/]*$/, '');
const pcFile = dv.pages(`"${parentFolder}"`).where(p => p.file.name.startsWith("PC -")).first();

const color = pcFile?.ability_colors?.strength || "#0892D0";

dv.paragraph(`
  <div style="font-size: 40px; font-weight: bold; line-height: 0.9; padding: 0; margin: -20px 0px 0px 0px; text-align: centre;">
    <div style="color: ${color}; padding: 0; margin: 0;">${pcFile?.strength || "?"}</div>
  </div>
`);
```
