---
dg-home: true
dg-publish: true
dg-pinned: true

cssclasses:
  - cards
coverImage: "[[attachments/rappy smile png.png]]"
thumbnail: "[[attachments/thumbnails/resized/b4acf603be96c762d06b7bc5d7ece9d1_86cf658e.webp]]"
dg-content-classes: cards
---
# Have some things!
---

Welcome to **Whimsy Scoundrel**: a silly little project by LvK!
I'll add more proper text later on, but for now let's get some placeholder info going...
![[attachments/rappy smile png.png|286]]
# Links To Start With
---

* [[FAQ]] - Curious about anything? Click here
* [[Gallery of Sightings]] - View the collection!





# Most Recent Sightings In The Wild
---
Want to see [[Gallery of Sightings.md|more]]?  


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


