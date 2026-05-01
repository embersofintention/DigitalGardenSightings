---
tags:
tagline: (empty)
date:
created: 2026-04-23, 16:01
created_date: 2026, 04/23
created_time: 16:01
dg-publish: false
cssclasses:
dg-content-classes:
---

```dataviewjs
let result = await dv.query(`LIST FROM "Sightings In The Wild"`);
let values = result.value.values;
let embeds = values.map(p => "[" + dv.fileLink(p.path, true) + "](<" + p.path + ">)");
dv.el("p", embeds, { cls: "dataview-cards-deck" });
```
# Rappy Cards

```dataviewjs
let result = await dv.query(`
	LIST FROM "Sightings In The Wild"
	WHERE contains(characters, "Zu")
`);
let values = result.value.values;
let embeds = values.map(p => "[" + dv.fileLink(p.path, true) + "](<" + p.path + ">)");
dv.el("p", embeds, { cls: "dataview-cards-deck" });
```



> [!polaroid] hi
> ![[Zu-4.png]]

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent rhoncus turpis non consectetur sodales. Integer eget dui turpis. Nulla rhoncus elit quis diam tincidunt sagittis. Quisque varius neque vitae enim suscipit, in sodales justo convallis. Donec sit amet urna ac elit fermentum facilisis ullamcorper sed elit. Maecenas tempus tempus nisi sit amet volutpat.

> [!polaroid|right] Les Calanques
> ![[Zu-2.webp]]

Vivamus et purus nec neque volutpat efficitur vitae eget augue. Maecenas vel malesuada leo, nec ullamcorper elit. Vivamus maximus eros sit amet diam hendrerit, non viverra leo consectetur. Fusce interdum placerat eros cursus vulputate. Nunc vel placerat elit. Quisque rutrum tortor vitae quam mattis dapibus. Aliquam eu ornare nunc, eget gravida ipsum. In nec tincidunt nunc. Nunc et leo ac sem sodales porta. Praesent vulputate dignissim eros, et laoreet lorem ornare id.

> [!polaroid|left] Aurora
> ![[Aurora.jpg]]

Sed auctor vitae sapien mollis tincidunt. Aliquam consectetur nisi et semper tristique. Nam suscipit dolor auctor, consequat turpis ut, commodo neque. Sed finibus euismod pellentesque. Proin vitae sodales justo, eget facilisis nibh. Maecenas pulvinar condimentum pharetra. Integer a vehicula ante. Proin bibendum mi ligula, non elementum massa vulputate eget. Suspendisse maximus, orci eget congue tempor, augue dolor dictum tellus, eget luctus ante enim eu lacus. Sed a rutrum lectus. Phasellus turpis mi, semper convallis volutpat eu, rutrum ac justo. Suspendisse potenti.

---


> [!profile]+ Test
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








---