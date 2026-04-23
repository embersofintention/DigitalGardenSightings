---
dg-home: true
dg-publish: true
dg-pinned: true
cssclasses:
  - cards
coverImage: "[[attachments/thumbnails/resized/2026-04-17 - Zu- Whimsy at a Brewhouse-2.webp]]"
thumbnail: "[[attachments/thumbnails/resized/757fcbd95057ae7b840163d9252fc941_86cf658e.webp]]"
dg-content-classes: cards
---
# Have some things!
---

Welcome to **Whimsy Scoundrel**: a silly little project by LvK!
I'll add more proper text later on, but for now let's get some placeholder info going...




# Links To Start With
---

* [[FAQ]] - Curious about anything? Click here
* [[Gallery of Sightings]] - View the collection!





> [!comic]
>> [!comic-panel|bubble top left]
>> > ![[2026-04-17 - Zu- Whimsy at a Brewhouse-2.webp]]
>> 
>> KAY COOL
>
>> [!comic-panel|bubble top right]
>> > ![[attachments/thumbnails/resized/2026-04-20 - Phaedra- Fruit Waffle Prickle Friend-3.webp]]
>> 
>> YE NIFTY!
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


