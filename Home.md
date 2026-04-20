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
## So What is a Whimsy Scoundrel?

* This is the name I've given to my little **index card cutout characters** that I leave about town for folks to find.  

## And Who is LvK?

* That's me! Hi!  
* I'm the artist, and the goofball behind these silly lil' pals.  
* A very friendly dude with a colorful hobby

## But Who are these little critters?

* Most of the lil' guys I leave about are one of two characters:  

	* Rapscallien / "Rappy" -- the sweet little lion-adjacent critter
	* Zu Nug -- the mischief-making cat, and personal character of my wonderful partner





# Sightings In The Wild
---
Here are some of the lil' guys I've left around town for folks to find!

Have you spotted any of these?

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


