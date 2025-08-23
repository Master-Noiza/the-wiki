---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let category = ""
let rarity = ""
let habitat = ""
let origin = ""
let season = ""
let application = ""
let traits = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the plant?");
aliases = await tp.system.prompt("Aliases: other names?");
category = await tp.system.prompt("Category: Flower, Fungi, Fruit, Herb, Root?");
rarity = await tp.system.prompt("Rarity: Common, Uncommon, Rare, Very Rare, Legendary, Unique?");
habitat = await tp.system.prompt("Habitat: Arctic, Coastal, Desert, Forests, Grasslands, Hills, Jungle, Mountains, Swamps, Underdark, Underwater, Urban?");
origin = await tp.system.prompt("Origin: Natural, Magical, Mirror?");
season = await tp.system.prompt("Season: Spring, Summer, Fall, Winter, Special days only?");
application = await tp.system.prompt("Application: Ingest, smear, inhale?");
traits = await tp.system.prompt("Traits: Healing, Poison, Cooking, Spice, Nourishment, Brewing, Resistance to X, Enhancement of X?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["category"] = category;
  frontmatter["rarity"] = rarity;
  frontmatter["habitat"] = habitat;
  frontmatter["origin"] = origin;
  frontmatter["seasons"] = seasons;
  frontmatter["applications"] = applications;
  frontmatter["traits"] = traits;
  })
}, 200)

-%>

# `=this.name`

---
> [!infobox]
> 
> 
> ## **`=this.name`**
> 
> ![[Plant_Placeholder1.webp]]
> 
> ## - Facts -
> |  |  |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Category** | `=this.category` |
> | **Rarity** | `=this.rarity` |
> | **Habitat** | `=this.habitat` |
> | **Origin** | `=this.origin` |
> | **Traits** | `=this.traits` |

<br>

>[!quote| author clean] *"This is a quote"*
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


> [!NOTE|clean ttl-c no-i]- Mechanics
> Penalty to find
> Effects
