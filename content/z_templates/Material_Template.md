---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let category = ""
let rarity = ""
let location = ""
let origin = ""
let usage = ""
let appearance = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the material?");
aliases = await tp.system.prompt("Aliases: other names?");
category = await tp.system.prompt("Category: Rock, Ore, Metal, Wood, Animal, Plant, Mineral?");
rarity = await tp.system.prompt("Rarity: Common, Uncommon, Rare, Very Rare, Legendary, Unique?");
location = await tp.system.prompt("Location: Arctic, Coastal, Desert, Forests, Grasslands, Hills, Jungle, Mountains, Swamps, Underdark, Underwater, Urban?");
origin = await tp.system.prompt("Origin: Natural, Crafted, Magical, Mirror?");
usage = await tp.system.prompt("Usage: Building, Smithing, Alchemy, Trading?");
appearance = await tp.system.prompt("Appearance: Colour, Structure?)

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["category"] = category;
  frontmatter["rarity"] = rarity;
  frontmatter["location"] = habitat;
  frontmatter["origin"] = origin;
  frontmatter["usage"] = usage;
  frontmatter["appearance"] = appearance;
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
> |  |  |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Category** | `=this.category` |
> | **Rarity** | `=this.rarity` |
> | **Location** | `=this.location` |
> | **Origin** | `=this.origin` |
> | **Usage** | `=this.usage` |
> | **Appearance** | `=this.appearance` |

<br>

>[!quote| author clean] *"This is a quote"*
>The Quoted, at a place, at X day

<br>

## Basic Information:
- Description
- Important Details
- Location Details
- Usage
<br>

**Trait1:**
- Description

<Add more if applicable>

---

> [!column]
> 
>> [!error| no-i ttl-c] Harvestables:
>> 
>> **Loot1**
>> - Usage
>> <Add more if applicable>
>
>> [!error| no-i ttl-c] Lore & Myths:
>> 
>> **Lorefact or Myth**
>> - Description
>>
>> <Add more if applicable>

---


> [!NOTE|clean ttl-c no-i]- Mechanics
> Penalty to find
> Effects
