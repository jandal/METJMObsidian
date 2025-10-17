# Lost Mine of Phandelver - Campaign Dashboard

> **Campaign Status:** Active | **Session:** TBD | **Date:** TBD

---

## 🎭 Party Overview

```dataview
TABLE 
  character_name as "Character",
  class as "Class",
  level as "Lvl",
  race as "Race",
  armor_class as "AC",
  hit_point_maximum as "Max HP",
  passive_wisdom as "Perception"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
SORT character_name ASC
```

---

## ⚔️ Combat Quick Reference

```dataview
TABLE WITHOUT ID
  character_name as "Character",
  armor_class as "AC",
  initiative as "Init",
  speed as "Speed",
  hit_point_maximum as "HP"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
SORT initiative DESC
```

---

## 🎲 Ability Scores Matrix

```dataview
TABLE 
  character_name as "Name",
  strength + " (" + strength_modifier + ")" as "STR",
  dexterity + " (" + dexterity_modifier + ")" as "DEX",
  constitution + " (" + constitution_modifier + ")" as "CON",
  intelligence + " (" + intelligence_modifier + ")" as "INT",
  wisdom + " (" + wisdom_modifier + ")" as "WIS",
  charisma + " (" + charisma_modifier + ")" as "CHA"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
```

---

## 🛡️ Saving Throws Reference

```dataview
TABLE
  character_name as "Character",
  strength_save as "STR",
  dexterity_save as "DEX",
  constitution_save as "CON",
  intelligence_save as "INT",
  wisdom_save as "WIS",
  charisma_save as "CHA"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
```

---

## 🎯 Skills & Proficiencies

```dataview
TABLE
  character_name as "Character",
  skill_proficiencies as "Skill Proficiencies",
  proficiency_bonus as "Prof Bonus"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE skill_proficiencies
```

---

## 💬 Languages Known

```dataview
TABLE
  character_name as "Character",
  languages as "Languages"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE languages
```

---

## 🗡️ Party Weapons & Attacks

```dataview
TABLE WITHOUT ID
  character_name as "Character",
  attacks.name as "Weapon",
  attacks.attack_bonus as "Attack Bonus",
  attacks.damage as "Damage"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE attacks
FLATTEN attacks
```

---

## 📊 Experience & Progression

```dataview
TABLE
  character_name as "Character",
  level as "Current Level",
  experience_points as "XP",
  (300 - experience_points) as "XP to Level 2"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
```

---

## ✨ Special Features Summary

```dataview
LIST
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE character_name
```

Click on character names above to see full feature descriptions.

---

## 📝 Incomplete Character Details

```dataview
LIST
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE contains(string(this.file), "TODO")
```

---

## 📖 Session Notes

```dataview
TABLE 
  file.ctime as "Date Created",
  file.mtime as "Last Modified"
FROM "H:/Documents/Obsidian/DND/LMoP"
WHERE contains(file.name, "Session")
SORT file.ctime DESC
```

---

## 🎲 Quick Stats Comparison

**Highest AC:** 
```dataview
LIST armor_class
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE armor_class
SORT armor_class DESC
LIMIT 1
```

**Highest HP:**
```dataview
LIST hit_point_maximum
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE hit_point_maximum
SORT hit_point_maximum DESC
LIMIT 1
```

**Best Perception:**
```dataview
LIST passive_wisdom
FROM "H:/Documents/Obsidian/DND/LMoP/PCs"
WHERE passive_wisdom
SORT passive_wisdom DESC
LIMIT 1
```

---

## 🗺️ Campaign Resources

- [[PC - Jandal]] - Party Wizard
- Add more PC links here as you create them
- Add NPC tracker
- Add location notes
- Add quest log

---

*Last Updated: `$= dv.current().file.mtime`*
