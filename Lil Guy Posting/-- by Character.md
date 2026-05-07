---
aliases:
tags:
tagline: (empty)
date:
created: 2026-04-23, 13:37
created_date: 2026, 04/23
created_time: 13:37
dg-publish: true
cssclasses:
  - cards
  - img-grid
dg-content-classes: cards, img-grid
coverImage: "[[attachments/rappy whimsy sketch 2.png]]"
thumbnail: "[[attachments/thumbnails/resized/e284d2d6aea662dfd450952a1141e586_86cf658e.webp]]"
dataviewIgnore: true
---
# Whimsy By Character
> [!full-width-image] # 
> > ![[rappy whimsy sketch 2.png]]
---






---
## Rappy
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
WHERE contains(characters, "Rappy")
SORT created_date DESC




WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg






```






---
## Zu
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
WHERE contains(characters, "Zu")
SORT created_date DESC




WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg






```

---
## Phaedra
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
WHERE contains(characters, "Phaedra")
SORT created_date DESC




WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg






```


---

## Misc

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
WHERE contains(characters, "misc")
SORT created_date DESC




WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg






```
























---