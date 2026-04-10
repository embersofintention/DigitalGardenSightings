---
{"dg-publish":true,"permalink":"/src/site/notes/test-index/","tags":["gardenEntry"],"dg-note-properties":{"permalink":"/test-index/","tags":["gardenEntry"]}}
---


# AAAAAAAAAAAAAAAAAAhiAAAAAAAAAAAA
While we get everything all figured out, and also my head hurts

![placeholder rappy.png](/img/user/attachments/placeholder%20rappy.png)

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

[[Test Dataview Gallery\|Test Dataview Gallery]] <-link

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

Experimental Dataview Gallery: osfjdos
| Preview                                     | About                                                                                          |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| ![attachments/rappy smile png.png\|250](/img/user/attachments/rappy%20smile%20png.png)   | [[test art/Rappy Smile Test Post\|Rappy Smile Test Post]] \| test rappy smile               |
| ![attachments/placeholder rappy.png\|250](/img/user/attachments/placeholder%20rappy.png) | [[test art/Rappy Placeholder Test Post\|Rappy Placeholder Test Post]] \| another test Rappy |

{ .block-language-dataview}
---



Working Dataview Gallery: 
| Preview                                     | About                                                                                          |
| ------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| ![attachments/rappy smile png.png\|250](/img/user/attachments/rappy%20smile%20png.png)   | [[test art/Rappy Smile Test Post\|Rappy Smile Test Post]] \| test rappy smile               |
| ![attachments/placeholder rappy.png\|250](/img/user/attachments/placeholder%20rappy.png) | [[test art/Rappy Placeholder Test Post\|Rappy Placeholder Test Post]] \| another test Rappy |

{ .block-language-dataview}







Also how 'bout some **bold**, *italic*, and ~~strikethrough~~ mayhaps?
also [[test art/Rappy Smile Test Post\|links]] are neato, let's test those. 

Okay! Welp. Here's hoping these work!

...