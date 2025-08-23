---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title 
let name = ""
let aliases = ""
let type = ""
let location = ""
let inhabitants = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: What is it?");
aliases = await tp.system.prompt("Aliases: Other names?");
type = await tp.system.prompt("Type: Forest, Lake, Mountain, Plains, River, other?");
location = await tp.system.prompt("Location: where is it?")
inhabitants = await tp.system.prompt("Inhabitants: Who lives there?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["type"] = type;
  frontmatter["location"] = location;
  frontmatter["inhabitants"] = inhabitants;
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
> ![[Boiling_Ponds.webp]]
> 
> ## - Facts -
> |  |  |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Type** | `=this.category` |
> | **Location** | `=this.rarity` |
> | **Inhabitants** | `=this.habitat` |

> [!quote|author clean] *"This is the first Quote."*
> The Quoted, at place X, at time Y

> [!quote|author clean] *"This is the second Quote."*
> The Quoted, at place X, at time Y

<br>

## Basic Information:
- Description
- Features
- (answer this without using a bullet list)

---

