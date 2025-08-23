---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let category = ""
let rarity = ""
let size = ""
let habitat = ""
let social = ""
let intellect = ""
let speech = ""
let diet = ""
let behavior = ""
let origin = ""
let traits = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the Beast?");
aliases = await tp.system.prompt("Aliases: other names?");
category = await tp.system.prompt("Category: Animal, Beast, Construct, Elemental, Humanoid, Monstrosity, Plant, Spirit, Undead?");
rarity = await tp.system.prompt("Rarity: Plentiful (-1), Common (-2), Uncommon (-4), Rare (-6), Very Rare (-8), Legendary (-12), Unique??");
size = await tp.system.prompt("Size: Tiny, Small, Medium, Large, Huge, Gargantuan, Colossal");
habitat = await tp.system.prompt("Habitat: Arctic, Coastal, Desert, Forests, Grasslands, Hills, Jungle,  Mountains, Swamps, Underdark, Underwater, Urban, Freshwater, Ocean?");
social = await tp.system.prompt("Social: Solitary, Pack, Tribal?");
intellect = await tp.system.prompt("Intellect: None, Low, Average, High, Very High, Genius, Quasi Omnicient?");
speech = await tp.system.prompt("Speech: Yes, no, maybe?");
diet = await tp.system.prompt("Diet: Herbivore, Carnivore, Omnivore??");
behavior = await tp.system.prompt("Bahavior:?");
origin = await tp.system.prompt("Origin: Natural, Magical, Mirror?");
traits = await tp.system.prompt("Traits: Appearance, Features, Body Parts, Immunities, Resistances, Weaknesses, Poisonous, Amphibious, Capable of magic, etc.?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["category"] = category;
  frontmatter["rarity"] = rarity;
  frontmatter["size"] = size;
  frontmatter["habitat"] = habitat;
  frontmatter["social"] = social;
  frontmatter["intellect"] = intellect;
  frontmatter["speech"] = speech;
  frontmatter["diet"] = diet;
  frontmatter["behavior"] = behavior;
  frontmatter["origin"] = origin;
  frontmatter["traits"] = traits;
  })
}, 200)

-%>
# `=this.name`

> [!infobox]
> 
> 
> ## **`=this.name`**
> 
> ![[Plant_Placeholder1.webp]]
> 
> ## - Facts -
> | Type | Name |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Category** | `=this.category` |
> | **Rarity** | `=this.rarity` |
> | **Habitat** | `=this.habitat` |
> | **Size** | `=this.size` |
> | **Social Structure** | `=this.social` |
> | **Intellect** | `=this.intellect` |
> | **Speech** | `=this.speech` |
> | **Diet** | `=this.diet` |
> | **Behavior** | `=this.behavior` |
> | **Origin** | `=this.origin` |
> | **Traits** | `=this.traits` |

<br>

>[!quote| author clean] *"This is the first quote"*
>The Quoted, at a place, at X day

>[!quote| author clean] *"This is the second quote"*
>The Quoted, at a place, at X day

<br>

## Basic Information:
- Small Description
- Usage
<br>

**Trait1:**
- Description

**Trait2:**
- Description

---

> [!column]
> 
>> [!error| no-i ttl-c] Harvestables:
>>**Loot1**
>>- Usage
>>**Loot2**
>>- Usage
>
>> [!error| no-i ttl-c] Lore & Myths:
>> 
>>**Lorefact1**
>>- Description
>>**Myth1**
>>- Description

---