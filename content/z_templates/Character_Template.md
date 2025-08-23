---
{"publish":true,"title":"Character_Template","cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let race = ""
let culture = ""
let aliases = ""
let rank = ""
let allegiances = ""
let relations = ""
let location = ""
let age = ""
let eyes = ""
let hair = ""
let features = ""
let born = ""
let died = ""
let origin = ""
let residence = ""
let occupation = ""
let religion = ""
let relatives = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name?");
race = await tp.system.prompt("Race: What is it?");
culture = await tp.system.prompt("Culture: What is it?");
aliases = await tp.system.prompt("Aliases: other names?");
rank = await tp.system.prompt("Rank: General, King, Emperor, High Priest?");
allegiances = await tp.system.prompt("Allegiances: Guilds, Cults?");
relations = await tp.system.prompt("Relations: Allies, Enemies, Contacts?");
location = await tp.system.prompt("Location: Where are they right now?");
age = await tp.system.prompt("Age: How old are they?");
eyes = await tp.system.prompt("Eyes: Eye colour");
hair = await tp.system.prompt("Hair: Hair colour and style");
features = await tp.system.prompt("Features: Scars, mutations, quirks and perks");
born = await tp.system.prompt("Born: Birthday");
died = await tp.system.prompt("Died: Day of death");
origin = await tp.system.prompt("Origin: Where are they from?");
residence = await tp.system.prompt("Residence: Where are they from?");
occupation = await tp.system.prompt("Occupation: Whats their job?");
religion = await tp.system.prompt("Religion: Primary Faith?");
relatives = await tp.system.prompt("Relatives: Family members?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["race"] = race;
  frontmatter["culture"] = culture;
  frontmatter["aliases"] = aliases;
  frontmatter["rank"] = rank;
  frontmatter["allegiances"] = allegiances;
  frontmatter["relations"] = relations;
  frontmatter["location"] = location;
  frontmatter["age"] = age;
  frontmatter["eyes"] = eyes;
  frontmatter["hair"] = hair;
  frontmatter["features"] = features;
  frontmatter["born"] = born;
  frontmatter["died"] = died;
  frontmatter["origin"] = origin;
  frontmatter["residence"] = residence;
  frontmatter["occupation"] = occupation;
  frontmatter["religion"] = religion;
  frontmatter["relatives"] = relatives;
  })
}, 200)

-%>
# `=this.name`

---
> [!infobox]
> 
> 
> ## `=this.name`
> 
> ![[Marek_Hraldorn.webp]]
> 
> ## **- Facts -**
> |  |  |
> | ---- | ---- |
> | **Race** | `=this.race` |
> | **Culture** | `=this.culture` |
> | **Aliases** | `=this.aliases` |
> | **Rank/Title** | `=this.titles` |
> | **Allegiance** | `=this.allegiances` |
> | **Relations** | `=this.relations` |
> | **Location** | `=this.location` |
> 
> ## **- Description -**
> |  |  |
> | ---- | ---- |
> | **Age** | `=this.age` |
> | **Eyes** | `=this.eyes` |
> | **Hair** | `=this.hair` |
> | **Distinctive Features** | `=this.features` |
> 
> ## **- Biography -**
> |  |  |
> | ---- | ---- |
> | **Born** | `=this.born` |
> | **Died** | `=this.died` |
> | **Origin** | `=this.origin` |
> | **Residence** | `=this.residence` |
> | **Profession** | `=this.occupation` |
> | **Primary Belief** | `=this.religion` |
> | **Relatives & Relationships** | - |

> [!quote|author clean] This is the first quote
> The Quoted, at place x, at time y

> [!quote|author clean] This is the second quote
> The Quoted, at place x, at time y

<br>

## Basic Information:

Short, distinctive description

<br>

## Description:

- Appearance, Distinctive Features
- Characteristcs and Behavior
- Special Abilities
- Quirks

<br>

## Background:
- Origin and important details
- Aspects about them that are of importance

<br>

## Relationships, Allies & Enemies
- Summary of any known and important professional & personal relationships.
- Description of affiliated organizations and groups

<br>

## Abilities, Resources & Weaknesses
- Do they possess any special powers of note?
- Do they command any significant resources?
- Are there any weaknesses of note?

---

> [!column]
> 
>> [!bug|no-i ttl-c clean]- **Encounters**
>>
>> **Situation 1**
>> - What happened
>>
>> **Situation2**
>> - What else?
>
>> [!bug|no-i ttl-c clean]- **Secrets & Rumors**
>> 
>> **Secret1**
>> - Details
>>   
>> **Rumor2**
>> - Details

---