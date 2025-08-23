---
{"publish":true,"title":"Settlement_Template","cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let category = ""
let usage = ""
let location = ""
let nation = ""
let population = ""
let inhabitants = ""
let condition = ""
let governance = ""
let leaders = ""
let seat_of_power = ""
let relations = ""
let organizations = ""
let people = ""
let places = ""
let commerce = ""
let defence = ""
let religions = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of Settlement?");
aliases = await tp.system.prompt("Aliases: other names?");
category = await tp.system.prompt("Category: Hamlet, Village, Town, City, Metropolis, Fortress?");
usage = await tp.system.prompt("Function: Capital, Port, Trade-Hub, Fortress, Defence?");
location = await tp.system.prompt("Location: Continent, Country, Area");
nation = await tp.system.prompt("Nation: Which nation is it part of?");
population = await tp.system.prompt("Population: How many people?");
inhabitants = await tp.system.prompt("Inhabitants: Cultures, Classes, Casts, etc?");
condition = await tp.system.prompt("Condition: Thriving, Stable, Declining, Ruined, etc");
governance = await tp.system.prompt("Democracy, Oligarchy, Democracy, Dictatorship?");
leaders = await tp.system.prompt("Leaders: The People in power are:");
seat_of_power = await tp.system.prompt("Government building: Senate, Wizards tower, fortress?");
relations = await tp.system.prompt("Relations: Faction A (Ally), City B (Enemy)...");
organizations = await tp.system.prompt("Organizations: IMPORTANT Organizations");
people = await tp.system.prompt("People: IMPORTANT people");
places = await tp.system.prompt("Places: Important Locations, Wards and buildings");
commerce = await tp.system.prompt("Commerce: Free or regulated");
defence = await tp.system.prompt("Commerce: Important defensive structures and forces");
religions = await tp.system.prompt("Religions: Primary and secondary faith");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["category"] = category;
  frontmatter["usage"] = usage;
  frontmatter["location"] = location;
  frontmatter["nation"] = nation;
  frontmatter["population"] = population;
  frontmatter["inhabitants"] = inhabitants;
  frontmatter["condition"] = condition;
  frontmatter["governance"] = governance;
  frontmatter["leaders"] = leaders;
  frontmatter["seat_of_power"] = seat_of_power;
  frontmatter["relations"] = relations;
  frontmatter["organizations"] = organizations;
  frontmatter["people"] = people;
  frontmatter["places"] = places;
  frontmatter["commerce"] = commerce;
  frontmatter["defence"] = defence;
  frontmatter["religions"] = religions;
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
> | **Category** | `=this.category` |
> | **Function** | `=this.usage` |
> | **Location** | `=this.location` |
> | **Nation** | `=this.nation` |
> | **Population** | `=this.population` |
> | **Inhabitants** | `=this.inhabitants` |
> | **Condition** | `=this.condition` |
> | **Governance** | `=this.governance` |
> | **Leaders** | `=this.leaders` |
> | **Seat of Power** | `=this.seat_of_power` |
> | **Relations** | `=this.relations` |
> | **Organizations** | `=this.organizations` |
> | **People of Note** | `=this.people` |
> | **Places of Note** | `=this.places` |
> | **Economy** | `=this.commerce` |
> | **Defence** | `=this.defence` |
> | **Primary Religions** | `=this.religions` |
> 

<br>

> [!quote|author clean] *"This is the first Quote."*
> The Quoted, at place X, at time Y

> [!quote|author clean] *"This is the second Quote."*
> The Quoted, at place X, at time Y

<br>

## Basic Information:

Basic decription, summary and highlighting of details of note

<br>

## Governance:

- What is the governmental system?
- Who are its leaders and notable political groups?
- What is its relationship with other settlements or nations?

<br>

## Defences:

- Does it have walls? Are they fortified?
- Does it have fortifications? Which ones and where?

### Watch & Guard:

- What is the name of its law enforcement, and its defensive forces?
- Standing army or militia?
- How strict or relaxed is law enforcement?

### Magic:
- Is Magic banned, regulated or encouraged?
- Details

<br>

## Social:

[City] has a population of XX‚XXX. The majority are [race], with a significant number of [race] and [race], and enclaves of [race].

- Social Welfare: Indifferent or benevolent (Comes in shades)
- What is the overall social hierarchy and how do they interact?
- What is the general standard of living?

### Public Institutions:

- Who are the main social institutions and organizations and how do they interact?

<br>

## Culture:

- What are some of its unique cultural traditions or customs?
- What is the general attitude towards cultural diversity?

### Cultural Institutions:

- What are organizations or landmarks with cultural significance? 

### Celebrations:

- What are some of its festivals or holidays?

<br>

## Economy:

- Is the Economy regulated or free? (Comes in shades) A few details will do
- What are its primary industries?
- What are the primary exports and imports?
- Does it have trade connections?
- Is there a black market?

### Major Businesses:

- What are some of its notable financial institutions or businesses?

<br>

## Geography: 

Geography, Climate, Urban Structure

- What are its climate and surrounding terrain, and natural resources?
- How is it located in relation to other important locations, and routes?

### Urban Structure:

- How big is the city, and how is it divided?
- What are notable features or landmarks?
- What are its Wards?

<br>

## Law & Crime:

[City] has a [level] level of criminal activity. Most being [type of crime], or [type of crime].

- What is the overall crime rate?
- Does it have organized crime or any major criminal organizations operating in it?
- What are the dangerous areas, if any?

### Rule of Law

- How does its justice system work?
- What are some notable laws or policies?
- How are crimes handled and by whom?
- Reform or Punishment?

<br>

## Religion

- What is the attitude towards religion and religious diversity?


### Religions & Faiths

- What is the dominant religion?
- What are secondary, and minor religions?

### Temples & Shrines

- What are its religious buildings, organizations, or landmarks?

---

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