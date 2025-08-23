---
{"publish":true,"tags":[null],"cssclasses":""}
---

<%* 
let title = tp.file.title
let race = ""
let culture = ""
let society = ""
let governance = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

race = await tp.system.prompt("Race: Main Race?");
culture = await tp.system.prompt("Culture: Name of the Subcultures?");
society = await tp.system.prompt("Society: Fractured? Unified?");
governance = await tp.system.prompt("Governance: Monarch= Senate?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["title"] = title;
  frontmatter["name"] = name;
  frontmatter["race"] = race;
  })
}, 200)

-%>
> [!infobox]
> 
> 
> ## `=this.name`
> 
> ![[NPC_Placeholder 2.webp]]
> 
> ## **- Facts -**
> |  |  |
> | ---- | ---- |
> | **Race** | `=this.race` |
> | **Aliases** | xyz |
> | **Rank/Title** | RankX |
> | **Allegiance** | Organizations, etc |
> | **Location** | `VIEW[{Aufenthaltsort}][link]` |
> 
> ## **- Description -**
> |  |  |
> | ---- | ---- |
> | **Spezies** | [[The Races#RaceXYZ]] |
> | **Culture** | NameofCulture |
> | **Age** | 1234 years |
> | **Eyes** | Colour |
> | **Hair** | Colour & Style |
> | **Distinctive Features** | Scars, Body, etc |
> 
> ## **- Biography -**
> |  |  |
> | ---- | ---- |
> | **Born** | Date |
> | **Died** | Date |
> | **Origin** | `VIEW[{Herkunft}][link]` |
> | **Residence** | `VIEW[{Wohnort}][link]` |
> | **Profession** | `=this.Profession` |
> | **Primary Belief** | `=this.Glaube` |
> | **Relatives & Relationships** | [[Person A]] (Beziehung) |