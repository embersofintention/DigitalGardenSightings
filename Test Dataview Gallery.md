---
tags:
tagline: (empty)
date:
created: 2026-04-09, 16:17
created_date: 2026, 04/09
created_time: 16:17
dg-publish: true
---


Dataview Gallery Test: 

```dataview

TABLE WITHOUT ID 
EmbededCoverImg as "Preview", 
link(file.name) + " | " + tagline as "About"




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