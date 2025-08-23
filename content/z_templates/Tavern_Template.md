---
{"publish":true,"aliases":"O t h e r n a m e s i f r e l e v a n t","cssclasses":""}
---

<%* 
let title = tp.file.title
let name = ""
let aliases = ""
let quality = ""
let location = ""
let owner = ""
let staff = ""
let patrons = ""
let status = ""
let legality = ""

if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
} await tp.file.rename(title);

name = await tp.system.prompt("Name: Name of the tavern?");
aliases = await tp.system.prompt("Aliases: other names?");
quality = await tp.system.prompt("Quality: Poor, Low, Average, Good, Wealthy, Aristocratic plus any relevant small additions?");
location = await tp.system.prompt("Location: Country, City, General location, etc?");
owner = await tp.system.prompt("Owner: Person X");
staff = await tp.system.prompt("Staff: Person y,<br>Person z,...");
patrons = await tp.system.prompt("Patrons: Citizens, Travelers, Soldiers, Craftsmen, Workers, Artists, Nobles, Criminals, Others?, just everyone?");
status = await tp.system.prompt("Status: In Operation/Closed?");
legality = await tp.system.prompt("Legality: Official/Unofficial?");

setTimeout(() => {
  app.fileManager.processFrontMatter(tp.config.target_file, frontmatter => {
  frontmatter["name"] = name;
  frontmatter["aliases"] = aliases;
  frontmatter["quality"] = quality;
  frontmatter["location"] = location;
  frontmatter["owner"] = owner;
  frontmatter["staff"] = staff;
  frontmatter["patrons"] = patrons;
  frontmatter["status"] = status;
  frontmatter["legality"] = legality;
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
> ![[Tavern_Placeholder.webp]]
> 
> ## - Facts -
> |  |  |
> | ---- | ---- |
> | **Aliases** | Other names if relevant |
> | **Quality** | Poor, Low, Average, Good, Wealthy, Aristocratic plus any relevant small additions |
> | **Location** | Country, City, General location, etc |
> | **Owner** | Person X |
> | **Staff** | Person y,<br>Person z,... |
> | **Patrons** | Citizens, Travelers, Soldiers, Craftsmen, Workers, Artists, Nobles, Criminals, Others?, just everyone? |
> | **Status** | In Operation/Closed |
> | **Legality** | Official/Unofficial |

<br>

>[!quote| author clean] *"This is a quote"*
>The Quoted, at a place, at X day

>[!quote| author clean] *"This is another quote"*
>The Quoted person z, at y place, at X day

<br>

## Description:
-
-

<br>

## Location:
-
-

<br>

## Menu:

> [!column]
>> [!info| clean no-i ttl-c] Food:
>> 
>> **Daily Soup:** 
>> - Soup/stew + possibly bread: Price
>>
>> **Breakfast:** 
>> - Dish 1: Price 
>> - Dish 2: Price 
>> - Dish 3: Price
>>
>> **Lunch:**
>> - Dish 1: Price
>> - Dish 2: Price
>> - Dish 3: Price
>>
>> **Dinner:**
>> - Dish 1: Price
>> - Dish 2: Price
>> - Dish 3: Price
>>
>> **Lunch Menu:**
>> - Menu (feel free to be creative): Price
>>
>> **Dinner Menu:**
>> - Menu (feel free to be creative): Price:
>
>> [!note| clean no-i ttl-c] Drink:
>> 
>> **Water & Non-Alcoholic:**
>> - Drink (feel free to be creative): Price per glass, Price per carafe/bottle
>> - <Add more>
>>
>> **Hot Drinks:**
>> - Drink (feel free to be creative): Price per cup, Price per pot
>> - <Add more>
>>
>> **Wine & Beer:**
>> - Drink (feel free to be creative): Price per mug/glass, Price per carafe/bottle/keg
>> - <Add more>
>>
>> **Spirits:**
>> - Drink (feel free to be creative): Price per shot, Price per bottle
>> - <Add more>

<br>

## Accommodation:

- **Single Room**: Price per night
- **Double Room**: Price per night
- **Dormitory <only up to good quality>:** Price per night
- Possibly add more accommodations, e.g., honeymoon suite, flea-infested hayloft, cabin on the grounds, etc.
<br>
- **Stable (If available):** Price per night including/excluding feeding, if not available, provide a reason why.

<br>

## Additional Offerings<If Available>:

- **Hot Bath:** Price and quality/description

**Tobacco:**
- Plain Tobacco: Price per 1/4 pound
- Spiced Tobacco: Price per 1/4 pound
- <Possibly other smoking products>

<If other special things/activities are offered (feel free to be creative):>
- **Offering:** Description & Price

<br>

## Staff:

**Owner:** Name and description

**Innkeeper:** Name and description (If different from the owner)

**Cook/Chef:** Name and description

**Serving Staff:**

<Other Employees>

<br>

## History:

<br>

## Rumors and Particularities: