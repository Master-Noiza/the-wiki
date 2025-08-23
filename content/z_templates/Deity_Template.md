---
{"publish":true,"cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let organisations = ""
let rank = ""
let symbol = ""
let portfolio = ""
let followers = ""
let relations = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the god?");
aliases = await tp.system.prompt("Aliases: other names?");
organisations = await tp.system.prompt("Organisations: Cults, religions, etc");
rank = await tp.system.prompt("Rank: Major, Minor, Demigod, Other?");
symbol = await tp.system.prompt("Symbol: What is it?");
portfolio = await tp.system.prompt("Portfolio: War, Agriculture, Oceans?");
followers = await tp.system.prompt("Followers: Workers, Merchants, Warriors?");
relations = await tp.system.prompt("Relations: God A (Ally), God B (Enemy)...");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["organisations"] = organisations;
  frontmatter["title"] = title;
  frontmatter["rank"] = rank;
  frontmatter["symbol"] = symbol;
  frontmatter["portfolio"] = portfolio;
  frontmatter["followers"] = followers;
  frontmatter["relations"] = relations;
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
> ![[NPC_Placeholder.jpg]]
> 
> ## - Facts -
> | Type | Name |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Rank** | `=this.rank` |
> | **Aspects** | [The Creator](../3.%20Gods%20&%20Religion/3.%20The%20Trinity/2.%20The%20Creator.md), <br>[The Preserver](../3.%20Gods%20&%20Religion/3.%20The%20Trinity/3.%20The%20Preserver.md), <br>[The Destroyer](../3.%20Gods%20&%20Religion/3.%20The%20Trinity/4.%20The%20Destroyer.md) |
> | **Aspect of** | `=this.aspect_of` |
> | **Portfolio** | `=this.portfolio` |
> | **Followers** | `=this.followers` |
> | **Organisations** | `=this.organisations` |
> | **Symbols** | `=this.symbol` |
> | **Godly Relations** |  |
> 


> [!quote|author clean] *"When they came, they came with shining steel and promises of peace. They left with Arkhold's coin and sons, but the north is ours yet. What the Empire forgets, Arkhold remembers."*
> Elara of the Council of Nine, Reflections on the Northern Wars

> [!quote|author clean] *"The north is cold and cruel, and it’s easy to lose faith. But in Arkhold, with the Nine as our witness, we are as much stone as the walls we defend."*
> City Watchman Mirdan, in conversation at the North Gate

<br>

## Basic Information:
- Which Aspects of the mundane and supernatural does the deity govern?
- Summary of the most important aspects
- What are their general characteristics?  
- (answer this without using a bullet list)

<br>

## Symbolism:
How is he/she depicted in art and/or writing?

In which form (if at all) does he/she show themselves in the mortal world?
(answer this without using a bullet list)

**Holy Symbol:**
- e.g. **Cross**, short despription

**Holy Color:**
- e.g. **White**, short despription

**Holy Number:**
- e.g. **One**, short despription

**Holy Animal/Beast:**
- e.g. **Pidgeon**, short despription

<br>

## Ideals:
4 Examples of the ideals & tenets of the deity.

**"Title"**

- Short description

**"Title"**

- Short description

**"Title"**

- Short description

**"Title"**

- Short description

---

## Proverbs, Chants & Prayers:

- 
- 
- 
- 

---

>[!bug|no-i txt-c ttl-c] Common Prayer to the deity:
>
>Prayer  

---

## Myths & Deeds:
>[!Warning| clean no-i] *"Title1"*
> Write one or more well-known storys such as a myth or deed. Especially useful if there are lessons to be drawn from the stories that can be taught to their followers. Title the story as well. It can either be a Cautionary tale or not.
---
>[!Warning| clean no-i] *"Title2"*
> Write one or more well-known storys such as a myth or deed. Especially useful if there are lessons to be drawn from the stories that can be taught to their followers. Title the story as well. It can either be a Cautionary tale or not.
---