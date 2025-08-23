---
{"publish":true,"title":"Nation_Template","cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let location = ""
let system = ""
let ruler = ""
let capital = ""
let cities = ""
let places = ""
let religions = ""
let traits = ""
let races = ""
let relations = ""
let organizations = ""
let commerce = ""
let defence = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the nation?");
aliases = await tp.system.prompt("Aliases: other names?");
location = await tp.system.prompt("Location: Continent, Climate?");
system = await tp.system.prompt("System: Monarchy, Dictatorship, Republic, Democracy?");
ruler = await tp.system.prompt("Ruler: Name, Type of ruler (Emperor, King, etc)");
capital = await tp.system.prompt("Capital: What is it?");
cities = await tp.system.prompt("Cities: Settlements of Note?");
places = await tp.system.prompt("Places: Important Locations and buildings");
religions = await tp.system.prompt("Religions: Primary & Secondary Religions");
traits = await tp.system.prompt("Traits: Values and things they strive for?");
races = await tp.system.prompt("Races: Majority and Minorities");
relations = await tp.system.prompt("Relations: Faction A (Ally), City B (Enemy)...");
organizations = await tp.system.prompt("Organizations: IMPORTANT Organizations");
commerce = await tp.system.prompt("Commerce: Free or regulated, Major Trading");
defence = await tp.system.prompt("Commerce: Important defensive structures and forces");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["location"] = location;
  frontmatter["system"] = system;
  frontmatter["ruler"] = ruler;
  frontmatter["capital"] = capital;
  frontmatter["cities"] = cities;
  frontmatter["places"] = places;
  frontmatter["religions"] = religions;
  frontmatter["traits"] = traits;
  frontmatter["races"] = races;
  frontmatter["relations"] = relations;
  frontmatter["organizations"] = organizations;
  frontmatter["commerce"] = commerce;
  frontmatter["defence"] = defence;
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
>![[castle.webp]]
> 
> ## - Overview -
> |  |  |
> | ---- | ---- |
> | **Aliases** | `=this.aliases` |
> | **Location** | `=this.location` |
> | **Governing<br>System** | `=this.system` |
> | **Ruler** | `=this.ruler` |
> | **Capital** | `=this.capital` |
> | **Important<br>Cities** | `=this.cities` |
> | **Major<br>Religions** | `=this.religions` |
> | **Renowned<br>Traits** | `=this.traits` |
> | **Population** | `=this.races` |
> | **Relations** | `=this.relations` |
> | **Organizations** | `=this.organizations` |
> | **Places of Note** | `=this.places` |
> | **Commerce** | `=this.commerce` |
> | **Defence** | `=this.defence` |


> [!quote|author clean] *"This is the first Quote."*
> The Quoted, at place X, at time Y

> [!quote|author clean] *"This is the second Quote."*
> The Quoted, at place X, at time Y

<br>

## Basic Information:

Basic decription, summary and highlighting of details of note
Climate, Location, Short summary of current Affairs

<br>

## Governance & National Politics:

- What is the governmental system?
- Who are its leaders and notable political groups?
- What is its relationship with other nations?
- What are the important political bodies and institutions?

<br>

## Military:

- Is the Nation defensive, aggressive, expansionist?
- Does it have a strong military force?

<br>

## Social:

- What is the overall social hierarchy and how do they interact?
- Is there room for movement between social classes?
- What is the general standard of living?

### Public Institutions:

- Who are the main social institutions and organizations and how do they interact?

<br>

## Culture:

- What is the cultural identity, what are the dominant practises, values and traditions?
- What are some of its unique cultural traditions or customs?
- What is the general attitude towards cultural diversity?

### Cultural Institutions:

- What are organizations or landmarks with cultural significance? 

### Celebrations:

- What are some of its festivals or holidays?

<br>

## Commerce:

- What are its primary industries?
- Is the market free or regulated?

### Major Businesses:

- What are some of its notable financial institutions or businesses?

<br>

## Geography: 

Geography, Climate

- What are its climate, terrain and natural resources?
- How is it located in relation to other important nations, and routes?

### Urban Structure:

- What are some important and influential cities

<br>

## Law & Crime:

- What is the overall crime rate?
- Does it have organized crime or any major criminal organizations operating in it?
- What are the dangerous areas, if any?

### Rule of Law

- How does its justice system work?
- What are some notable laws or policies?
- How are crimes handled and by whom?

<br>

## Religion

- What are the most important faiths and religious identity?
- What is the attitude towards religion and religious diversity?

### Religions & Faiths

- What is the dominant religion?
- What are secondary, and minor religions?

### Temples & Shrines

- What are its religious buildings, organizations, or landmarks?

---

## International Relations:

- The kingdom or nation's relationships with neighboring countries, allies, and enemies

## Local History

<br>

### <center> - Founding (Date) - <center/>

Why, when, and how was its foundation?

### <center> - Event (Date) - <center/>

Description / Key Points about the event

---

## Myths & Deeds:

>[!Warning| clean no-i] *"Title1"*
> Write one or more well-known storys such as a myth or deed.


---
>[!Warning| clean no-i] *"Title2"*
> Write one or more well-known storys such as a myth or deed.


---