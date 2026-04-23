---
tags:
tagline: (empty)
date:
created: 2026-04-23, 16:01
created_date: 2026, 04/23
created_time: 16:01
dg-publish: false
cssclasses:
  - dataview-cards-deck
dg-content-classes: dataview-cards-deck
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















---