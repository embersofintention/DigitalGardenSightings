---
tags:
tagline: (empty)
date:
created: 2026-04-22, 18:46
created_date: 2026, 04/22
created_time: 18:46
cssclasses:
  - pws-tables-cards
  - pws-tables-cards-ccg
dg-pinned: false
dg-content-classes: pws-tables-cards, pws-tables-cards-ccg
---

# Whimsy Scoundrel Sightings
---
Here are some of the lil' guys I've left around town for folks to find!

Have you found any of these? 

## Collection of Whimsy
Hover your mouse over the top text to preview, or click to see more!

```dataview

TABLE WITHOUT ID 

EmbededCoverImg
	as "background",

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



```












---
