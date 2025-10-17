---
excalidraw-border-color: transparent
excalidraw-default-mode: view
---
```dataviewjs
const parentFolder = dv.current().file.folder.replace(/\/[^/]*$/, '');
const pcFile = dv.pages(`"${parentFolder}"`).where(p => p.file.name.startsWith("PC -")).first();
const color = pcFile?.primary_color || "#06A77D";
// Array of your four proficient skills
const proficientSkills = pcFile?.skill_proficiencies || [];
const skillToCheck = "Acrobatics";
// Change this per databit
const isChecked = proficientSkills.includes(skillToCheck);
dv.paragraph(`
<div style="display: inline-block; width: 32px; height: 32px; border: 3px solid ${color}; border-radius: 50%; background-color: ${isChecked ? color : 'transparent'}; box-sizing: border-box;"></div>
`)
```
