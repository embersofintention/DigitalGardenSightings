---
tags:
tagline: (empty)
date:
created: 2026-04-09, 16:17
created_date: 2026, 04/09
created_time: 16:17
dg-publish: true
cssclasses:
  - pws-tables-cards
---


Dataview Gallery Test, using Jon Lee's Pub Wrap stuff



```dataview

TABLE WITHOUT ID 

EmbededCoverImg 
	as "Preview", 


link(file.name) 
	  as "Link",

tagline
	as "tagline"




FROM "test art" AND !"_Templates" AND !"index"
SORT created_date

WHERE file.name != this.file.name AND coverImage
FLATTEN choice(typeof(coverImage)="link",
    embed(link(meta(
        choice(
            typeof(coverImage)="link",
                coverImage, this.file.link
        )
    ).path, "250")), "![](" + coverImage + ")") AS EmbededCoverImg

```












.