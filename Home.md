---
dg-home: true
dg-publish: true
dg-pinned: true
cssclasses:
  - cards
coverImage: "[[attachments/Logos/whimsy scoundrel logo wip 2.png]]"
thumbnail: "[[attachments/thumbnails/resized/39fdf70f2df74e0900390130ed3414bc_86cf658e.webp]]"
dg-content-classes: cards
---

![[whimsy scoundrel logo wip 2.png]]

# Have some things!
---

Welcome to **Whimsy Scoundrel**: a silly little project by LvK!
I'll add more proper text later on, but for now let's get some placeholder info going....




# Links To Start With
---

* [[FAQ]] - Curious about anything? Click here
* [[Gallery of Sightings]] - View the collection!
* [[-- by Character|Character Gallery]] - Sorted by character

> [!comic] Placeholder Nonsense Hello
>> [!comic-panel|bubble top left]
>> > ![[2026-04-17 - Zu- Whimsy at a Brewhouse-2.webp]]
>> 
>>  [[Gallery of Sightings|Gallery]] ok
>
>> [!comic-panel|bubble top right]
>> > ![[attachments/thumbnails/resized/2026-04-20 - Phaedra- Fruit Waffle Prickle Friend-3.webp]]
>> 
>> Go look at it
>







# Most Recent Sightings In The Wild
---

```dataview

TABLE WITHOUT ID 

EmbededCoverImg 
	as "Thumbnail", 


"**" + link(file.path, header) + "**"
	  as "Link",

"**" + created_date + "**"
	+ " -- "
	+ description
	as "info",

"**Left at**"
	+ ": "
	+ leftAt
	as "Left At"




FROM "Sightings In The Wild" AND !"_Templates" AND !"index"
WHERE dataviewIgnore != true
SORT created_date DESC


WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg

LIMIT 9


```
> [!clue|tape-b paper-d]+ Want More Whimsy?
> Head to the [[Gallery of Sightings.md|Gallery of Sightings]] and look around!





# Please Note:  This is a work in progress!!
---

## Testing Various Stuff:

### Formatting



> This is a test quote

- [ ] This is a test checkbox
- [x] And this one's checked

```
oh hey look! A test code block!
```




# header 1
## header 2

### header 3

#### header 4

##### header 5


