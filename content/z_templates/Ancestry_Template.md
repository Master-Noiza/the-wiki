---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let type = ""
let ancestry = ""
let adult = ""
let lifespan = ""
let height = ""
let weight = ""
let weaving_discipline = ""
let society = ""
let governance = ""
let speech = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the race?");
aliases = await tp.system.prompt("Aliases: other names?");
type = await tp.system.prompt("Type: Semi/Sentient, Humanoid, Bestial?");
ancestry = await tp.system.prompt("Ancestry: Motherspecies?");
adult = await tp.system.prompt("Adulthood: Age, oly the number!");
lifespan = await tp.system.prompt("Lifespan: Lifespan, only the number!");
height = await tp.system.prompt("Height: Height in Meters?");
weight = await tp.system.prompt("Weight: Weight in Kilos?");
weaving_discipline = await tp.system.prompt("Discipline: None, Elementalism?");
society = await tp.system.prompt("Society: Most common type of society?");
governance = await tp.system.prompt("Governance: Emperor, Elector Count, President?");
speech = await tp.system.prompt("Speech: How is the Language called?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["type"] = type;
  frontmatter["ancestry"] = ancestry;
  frontmatter["adult"] = adult;
  frontmatter["lifespan"] = lifespan;
  frontmatter["height"] = height;
  frontmatter["weight"] = weight;
  frontmatter["weaving_discipline"] = weaving_discipline;
  frontmatter["society"] = society;
  frontmatter["governance"] = governance;
  frontmatter["speech"] = speech;
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
> ![[NPC_Placeholder.webp]]
> 
> ## - Facts -
> |  |  |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Type** | `=this.type` |
> | **Ancestry** | `=this.ancestry` |
> | **Age** | `=this.adult` Years (Adult) <br>`=this.lifespan` Years (Lifespan) |
> | **Height** | `=this.height` |
> | **Weight** | `=this.weight` |
> | **Weaving<br>Discipline** | `=this.weaving_discipline` |
> | **Society** | `=this.society` |
> | **Governance** | `=this.governance` |
> | **Speech** | `=this.speech` |

<br>

>[!quote| author clean] *"This is the first quote"*
>The Quoted, at a place, at X day

>[!quote| author clean] *"This is the second quote"*
>The Quoted, at a place, at X day

<br>

## Basic Information:
- Small Description
- Summary of important details

<br>

## Current Affairs:
- Politics, current situation, important details

<br>

## Racial Traits:

**Trait1:**
- Description

**Trait2:**
- Description

---

## Myths and History:

**Fact1:**
- Description

**Myth2:**
- Description

---