---
tags:
  - DBT
  - mental-health
  - art
tagline: (empty)
created: <% tp.file.creation_date("YYYY-MM-DD, HH:mm") %>
created_date: <% tp.file.creation_date("YYYY, MM/DD") %>
created_time: <% tp.file.creation_date("HH:mm") %>
coverImage:
thumbnail:
header:
description:
dg-publish:
dg-content-classes: cards, img-grid
cssclasses:
  - cards
  - img-grid
dbt-module:
  - placeholder
---
<%*
const dbtModules = [
  "Mindfulness",
  "Distress Tolerance",
  "Interpersonal Effectiveness",
  "Emotional Regulation"
];

let dbtModule = await tp.system.suggester(
  dbtModules,
  dbtModules,
  false,
  "Choose a DBT module"
);

let header = await tp.system.prompt('DBT Skill? (header)');
let description = await tp.system.prompt('Add brief context (description)');
let tagsInput = await tp.system.prompt('Any additional tags? Comma-separated. (added to tags)');
let charTags = tagsInput.split(',').map(t => t.trim()).filter(t => t.length > 0);

const file = tp.file.find_tfile(tp.file.path(true));
await app.fileManager.processFrontMatter(file, (frontmatter) => {
  frontmatter.header = header;
  frontmatter.description = description;
  frontmatter["dbt-module"] = dbtModule;

  const existingTags = Array.isArray(frontmatter.tags)
    ? frontmatter.tags
    : frontmatter.tags
      ? [frontmatter.tags]
      : [];

  frontmatter.tags = [...new Set([...existingTags, ...charTags])];
});

await tp.file.rename(tp.date.now("YYYY-MM-DD") + " - " + dbtModule + " - " + header);
%>


# <%- header %>



<%- description %>









---