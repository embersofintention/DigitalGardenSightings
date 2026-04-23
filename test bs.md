---
coverImage: "[[attachments/test bs-1.png]]"
thumbnail: "[[attachments/thumbnails/resized/024884ea9ba6d532b93b363fd38f92eb_86cf658e.webp]]"
---
![[test bs-1.png]]


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


















```
An example of how to group table results

dataview
TABLE WITHOUT ID
  rows.EmbededCoverImg AS Thumbnail,
  rows.Link AS Link,
  rows.Info AS Info,
  rows["Left At"] AS "Left At"
FROM "Sightings In The Wild"
WHERE file.name != this.file.name AND coverImage AND characters
FLATTEN characters AS characterFlat
FLATTEN choice(
  typeof(coverImage) = "link",
  embed(link(meta(coverImage).path, "250")),
  "![](" + coverImage + ")"
) AS EmbededCoverImg
FLATTEN "**" + link(file.path, header) + "**" AS Link
FLATTEN "**" + created_date + "** -- " + description AS Info
FLATTEN "**Left at**: " + leftAt AS "Left At"
GROUP BY characterFlat
SORT rows.created_date DESC

```

























# Callouts
styled via neat css snippets I added

> [!masonry]
> ![[Zu-5.png]]
> ![[Zu-2.png]]
> ![[Zu-3.png]]

> [!conversation]
> **Rappy**
> My knees hurt 
> 
> **Zu**
> Also you're a butt
> 
> **Rappy**
> That's fucking rude. 

---

> [!profile]+
>  ![[Zu-5.png]]
> 
> A whimsical little shitlort what can I say I love him lol


 > [!clue|tape-b paper-c]+ Rapscallien
The artist's internal experience, personified
>


> [!profile]+
>  ![[attachments/test bs-1.png|Rappy]]
>  
> ---
>  * **Name**: Rapscallien / "Rappy"
>  * **Pronouns**: They/them
> 
> ---
> 
> A whimsical little shitlort what can I say I love him lol




> [!clue|tape-b paper-d]+ Lad
>> [!profile]+ Rapscallien
>>  ![[attachments/Rappy-1.png]]
>>  The Artist's Internal Experience, Personified
>> 
>> ---
>>  * **Name**: Rapscallien / "Rappy"
>>  * **Pronouns**: They/them
>> 
>> ---
>> Raucous and rambunctious, these little doodle creatures are *living personifications* of all those thoughts and feelings that go unsaid.





Raucous and rambunctious, these little doodle creatures are *living personifications* of all those thoughts and feelings that go unsaid.

-



> [!pinned|medium]+ hi
> osajdfosjfdf



> [!full-width-image|grayscale red] # Full width image

> [!full-width-image] Hi
 ![[attachments/Rappy-1.png]]
> osjdfosjf





















-