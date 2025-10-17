# Character Sheet - Inline Dataview Template

> Copy these text snippets into Excalidraw text boxes to create a dynamic character sheet!

---

## Basic Information
```
Character: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").character_name`
Class: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").class` | Level: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").level`
Race: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").race`
Background: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").background`
Alignment: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").alignment`
```

---

## Ability Scores (Copy each separately)

**Strength:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").strength` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").strength_modifier`)
```

**Dexterity:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").dexterity` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").dexterity_modifier`)
```

**Constitution:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").constitution` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").constitution_modifier`)
```

**Intelligence:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").intelligence` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").intelligence_modifier`)
```

**Wisdom:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").wisdom` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").wisdom_modifier`)
```

**Charisma:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").charisma` (`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").charisma_modifier`)
```

---

## Combat Stats

**Armour Class:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").armor_class`
```

**Initiative:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").initiative`
```

**Speed:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").speed` ft
```

**Hit Points:**
```
Max: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").hit_point_maximum`
Current: [Write in manually or use metadata]
```

**Hit Dice:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").total_hit_dice`
```

---

## Saving Throws

```
STR: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").strength_save`
DEX: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").dexterity_save`
CON: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").constitution_save`
INT: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").intelligence_save`
WIS: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").wisdom_save`
CHA: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").charisma_save`
```

---

## Skills (Proficient Only)

```
Arcana: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").arcana`
History: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").history`
Investigation: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").investigation`
Medicine: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").medicine`
```

**Passive Perception:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").passive_wisdom`
```

**Proficiency Bonus:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").proficiency_bonus`
```

---

## Attacks

**Attack 1:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[0].name`
Hit: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[0].attack_bonus`
Damage: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[0].damage`
```

**Attack 2:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[1].name`
Hit: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[1].attack_bonus`
Damage: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[1].damage`
```

**Attack 3:**
```
`$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[2].name`
Hit: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[2].attack_bonus`
Damage: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").attacks[2].damage`
```

---

## Experience

```
XP: `$= dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md").experience_points`
```

---

## 🎨 How to Use This in Excalidraw:

1. **Create a new Excalidraw drawing** (Right-click folder > New Excalidraw drawing)
2. **Design your character sheet** with boxes, circles, and layout
3. **Add text elements** where you want dynamic data
4. **Copy-paste** the inline Dataview queries from above into those text boxes
5. **View in Reading Mode** to see the data populate!

### 📝 Tips:

- The inline queries work in **Reading/Preview mode** only
- Keep text boxes organised and aligned with your drawn elements
- Use Excalidraw's grouping feature to keep related elements together
- You can style the text (bold, colours, sizes) and the queries will still work
- Create shapes for "bubbles" around your stats (circles for ability scores work great!)

### 🔄 Alternative: Excalidraw with Embedded Notes

You can also:
1. Create the Excalidraw drawing
2. In the Excalidraw file's markdown (toggle with Ctrl/Cmd + Shift + E)
3. Add full Dataview TABLE queries below your drawing

This gives you both a visual sheet AND dynamic tables underneath!

---

## 🎯 Shortcut Version (for quick text boxes):

If the full path is too long, create a simple variable reference at the top of your Excalidraw note:

```javascript
<%*
const jandal = dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md");
%>
```

Then use:
```
Name: `$= jandal.character_name`
AC: `$= jandal.armor_class`
```

Much cleaner!
