---
coverImage: "[[Zu-5.png]]"
thumbnail: "[[attachments/thumbnails/resized/2b56020409e4b38877f696f15f3c8a74_86cf658e.webp]]"
tags:
tagline: (empty)
date:
created: 2026-04-23, 15:20
created_date: 2026, 04/23
created_time: 15:20
dg-publish: false
cssclasses:
  - cards
  - img-grid
  - dataview-cards-deck
dg-content-classes: cards, img-grid
---






# Zu!

> [!profile]+ Zu
>  ![[Zu-5.png]]
> 
> A whimsical little shitlort what can I say I love him lol


> [!cards-deck] The Bean
> 
> ![[Zu-5.png]]








## Gallery
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