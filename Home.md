---
dg-home: true
dg-publish: true
dg-pinned: true
cssclasses:
  - cards
  - headings-rainbow
coverImage: "[[attachments/Logos/whimsy scoundrel logo wip 2.png]]"
thumbnail: "[[attachments/thumbnails/resized/39fdf70f2df74e0900390130ed3414bc_86cf658e.webp]]"
dg-content-classes:
  - cards
  - img-grid
  - font-mansalva
---

![[whimsy scoundrel logo wip 2.png]]
>[!pinned]+ Site Is Heavily Under Construction
>expect weird stuff all over the place for now.
>
>Seriously, 'til I'm ready to consider this shareable, I'm gonna be tossing weird placeholder nonsense all over the place.  Expect a mess, but feel free to poke around and enjoy the chaos haha


---
# Imagination, Good Vibes and Whimsy
---
>[!fwi|wide no-title] Sweet! 
>![[attachments/2026-04-16-1734--Zu Ice Cream 1.jpg]]


.
.
.
## So What Is a Whimsy Scoundrel?
> [!polaroid|right] Phaedra (porcupine)
> ![[attachments/2026-04-23 - Phaedra- Found a new fave-1.png]]

**It's what I call my little index card critters!**
* often created on the spot, designed to be interacting with something in the environment
* left for others to find, with friendly little notes on the back
* Done as a silly lil' way to bring some playfulness and whimsy into each day!

(The term can also refer to both the concept as a *fun little artistic movement*, and a *name for folks who do it too!*)

---

> [!polaroid|left] Zu / Nug (cat)
> ![[Zu-5.png]]
## Why I Do The Thing

Well... Life is rough. We're stuck running around this way and that, all caught up in a relentless grind that's often pretty thankless.  And for a lot of folks, it's getting harder and harder to find those *little moments in the day that leave us with a sense of genuine joy.*

But we don't have to accept this at face value -- **Why not create those moments ourselves**, and make things a little more interesting?  

It costs next to nothing, it's fun to do, and it has the potential to make a stranger's day.  Good things all around!

> [!polaroid] Rappy (Whoosh!)
> ![[attachments/2026-04-25 - Rappy- Whoooosh-1.jpg]]


>[!fwi|wide no-title] egads! 
> ![[banner-1.png]]




# Links For Now (while I'm getting stuff set up)
---
(Remember, this site is very much a work in progress. Everything is still a mess and not intended to be seen JUST yet, but click around if you'd like since you're here!)

* [[FAQ]] - Curious about anything? Click here
* [[Gallery of Sightings]] - View the collection!
* [[-- by Character|Character Gallery]] - Sorted by character
* ...Or maybe you'd like to [[Whimsy Questing|try out]] something like this yourself..?

> [!comic] Placeholder Nonsense Hello
>> [!comic-panel|bubble top left]
>> > ![[2026-04-17 - Zu- Whimsy at a Brewhouse-2.webp]]
>> 
>>  [[Gallery of Sightings|Gallery]] ok
>
>> [!comic-panel|bubble bottom right]
>> > ![[attachments/2026-04-20 - Phaedra- Fruit Waffle Prickle Friend-3.png]]
>> 
>> Go look at it
>







# Most Recent Sightings In The Wild
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
WHERE dataviewIgnore != true
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
> [!clue|tape-b paper-d]+ Want More Whimsy?
> Head to the [[Gallery of Sightings.md|Gallery of Sightings]] and look around!


> [!profile]+ Profile WIP Test Thing
>> > [!polaroid|right] Derp
>> ![[Rappy-1.png]]
>  
> ---
>  * **Name**: Rapscallien / "Rappy"
>  * **Pronouns**: They/them
> 
> ---
> 
> A whimsical little dingus what can I say I love him lol


# Please Note:  This is a work in progress!!
---

## Testing Various Stuff:

### Formatting

==highlights==

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


