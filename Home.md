---
dg-home: true
dg-publish: true
cssclasses:
  - cards
coverImage: "[[attachments/placeholder rappy.png]]"
thumbnail: "[[attachments/thumbnails/resized/db79e302df68799c485f3c2c5dc3be02_86cf658e.webp]]"
---
# 4/15 - I think the gallery works now??????

Settings are getting nailed down!
Plugins are plugin-ing! 
Template does template things!
Soon enough I'll be able to go through my stash and post these lil guys!

now I'm just messing with the gallery layout

![[placeholder rappy.png]]


# Test Gallery

```dataview

TABLE WITHOUT ID 

EmbededCoverImg 
	as "Preview", 


"**" + link(file.path, header) + "**"
	  as "Link",

"**" + created_date + "**"
	+ " -- "
	+ description
	as "info"




FROM "Art Posts" AND !"_Templates" AND !"index"
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

## Goals:
Once everything is connected properly and stuff publishes, here are the next orders of business:
* *add the actual art lol*
* Make the site pretty with a snazzy layout

## Steps to get there: 
* adding the plugins I use for general working-on-stuff-in-Obsidian
* Setting up to sync between local devices, so I can add art from wherever (heck yeah)
* changing vault settings so a few of the defaults don't drive me nuts
* other stuff but for now let's just see if this publishes

Wish me luck please, I am clueless but stubborn. :D


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


