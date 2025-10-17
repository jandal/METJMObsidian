# Generate Jandal Character Sheet with ExcalidrawAutomate

This is a DataviewJS script that generates a character sheet in Excalidraw using data from Jandal's file.

## How to Use:
1. Make sure you have Excalidraw plugin installed
2. Put this code in a note
3. Switch to Reading/Preview mode
4. The script will generate an Excalidraw drawing with Jandal's stats!

```dataviewjs
// Get character data
const charFile = dv.page("H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md");

// Initialize Excalidraw Automate
const ea = ExcalidrawAutomate;
ea.reset();

// Set styling
ea.style.strokeColor = "#1e1e1e";
ea.style.backgroundColor = "#f8f8f8";
ea.style.fillStyle = "solid";
ea.style.strokeWidth = 2;
ea.style.fontFamily = 1; // Virgil (hand-drawn style)
ea.style.fontSize = 20;

// Title
ea.style.fontSize = 32;
ea.addText(50, 20, `${charFile.character_name} the ${charFile.race} ${charFile.class}`);

// Character Info Box
ea.style.fontSize = 16;
ea.addRect(50, 80, 300, 120);
ea.addText(70, 100, `Level: ${charFile.level}`);
ea.addText(70, 130, `Background: ${charFile.background}`);
ea.addText(70, 160, `Alignment: ${charFile.alignment}`);

// Ability Scores - Create 6 circles
const abilityX = 400;
const abilityY = 80;
const spacing = 100;

const abilities = [
  {name: "STR", score: charFile.strength, mod: charFile.strength_modifier},
  {name: "DEX", score: charFile.dexterity, mod: charFile.dexterity_modifier},
  {name: "CON", score: charFile.constitution, mod: charFile.constitution_modifier},
  {name: "INT", score: charFile.intelligence, mod: charFile.intelligence_modifier},
  {name: "WIS", score: charFile.wisdom, mod: charFile.wisdom_modifier},
  {name: "CHA", score: charFile.charisma, mod: charFile.charisma_modifier}
];

let yPos = abilityY;
abilities.forEach(ability => {
  ea.addEllipse(abilityX, yPos, 80, 80);
  ea.style.fontSize = 12;
  ea.addText(abilityX + 20, yPos + 10, ability.name);
  ea.style.fontSize = 24;
  ea.addText(abilityX + 20, yPos + 30, `${ability.score}`);
  ea.style.fontSize = 14;
  ea.addText(abilityX + 20, yPos + 55, `(${ability.mod})`);
  yPos += spacing;
});

// Combat Stats Box
ea.style.fontSize = 16;
ea.addRect(50, 220, 300, 180);
ea.addText(70, 240, `AC: ${charFile.armor_class}`);
ea.addText(70, 270, `Initiative: ${charFile.initiative}`);
ea.addText(70, 300, `Speed: ${charFile.speed} ft`);
ea.addText(70, 330, `HP: ${charFile.hit_point_maximum}`);
ea.addText(70, 360, `Hit Dice: ${charFile.total_hit_dice}`);

// Proficiency
ea.addText(70, 420, `Proficiency Bonus: ${charFile.proficiency_bonus}`);
ea.addText(70, 450, `Passive Perception: ${charFile.passive_wisdom}`);

// Attacks
ea.style.fontSize = 18;
ea.addText(520, 400, "ATTACKS");
ea.style.fontSize = 14;

let attackY = 430;
if (charFile.attacks) {
  charFile.attacks.forEach(attack => {
    ea.addRect(520, attackY, 250, 60);
    ea.addText(530, attackY + 10, attack.name);
    ea.addText(530, attackY + 30, `To Hit: ${attack.attack_bonus}`);
    ea.addText(530, attackY + 50, `Damage: ${attack.damage}`);
    attackY += 70;
  });
}

// Create the drawing
await ea.create({
  filename: "Jandal Character Sheet",
  foldername: "H:/Documents/Obsidian/DND/LMoP/PCs"
});

dv.paragraph("✅ Character sheet generated! Check your PCs folder.");
```

---

## Alternative: Simple Embedded Approach

If the above doesn't work, try this simpler version that just displays the data below your hand-drawn sheet:

1. Create your character sheet drawing manually in Excalidraw
2. Save it as "Jandal Visual Sheet.excalidraw"
3. Create a new note with:

```markdown
# Jandal's Character Sheet

![[Jandal Visual Sheet.excalidraw]]

## Live Stats from Data File

```dataview
TABLE 
  character_name as "Character",
  class as "Class",
  level as "Level",
  armor_class as "AC",
  hit_point_maximum as "Max HP"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md"
```

### Ability Scores
```dataview
TABLE 
  strength as "STR",
  dexterity as "DEX",
  constitution as "CON",
  intelligence as "INT",
  wisdom as "WIS",
  charisma as "CHA"
FROM "H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md"
```

### Combat Stats
```dataview
LIST
  "AC: " + armor_class,
  "Initiative: " + initiative,
  "Speed: " + speed + " ft",
  "HP: " + hit_point_maximum
FROM "H:/Documents/Obsidian/DND/LMoP/PCs/PC - Jandal.md"
```
```

![[Pasted image 20251009132939.png]]