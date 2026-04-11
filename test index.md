---
dg-home: true
dg-publish: true
cssclasses:
---
# 4/10, 3:37pm edit While I break my brain trying to fix stuff
While we get everything all figured out, and also my head hurts

![[placeholder rappy.png]]

I'm trying to connect Neocities with Obsidian, so I can share a whole bunch of art I do.  

Currently, the setup I'm testing is using a plugin called Digital Garden.  At the moment it looks a bit more promising than Kiln, so here's hoping?

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


## A Few Test Thingies

[[Test Dataview Gallery]] <-link

> This is a test quote

- [ ] This is a test checkbox
- [x] And this one's checked

```
oh hey look! A test code block!
```


### Test Galleries
And what if we test a gallery in the page?


Base, Created with a code block:
```base
  filters:
    "!image_path.isEmpty()"
  views:
    - type: cards
      name: "Image Gallery"
      image: image_path
      cardSize: 250
      imageFit: cover
      imageAspectRatio: 1
      order:
        - file.name
        - tags
        - created_date
        - image_path
  
```

---

Experimental Dataview Gallery: MAYBE IT'LL WORK I DO NOT KNOW PLZ WORK OK
```dataview

TABLE WITHOUT ID 
EmbededCoverImg 
	as "Preview", 


link(file.name) 
	+ " | " 
	+ tagline 
	  as "About"




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
---



Working Dataview Gallery: 
```dataview

TABLE WITHOUT ID 
EmbededCoverImg as "Preview", 
link(file.name) 
	+ " | " 
	+ tagline 
	  as "About"




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







Also how 'bout some **bold**, *italic*, and ~~strikethrough~~ mayhaps?
also [[Rappy Smile Test Post|links]] are neato, let's test those. 

Okay! Welp. Here's hoping these work!

...