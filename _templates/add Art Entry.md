---
tags:
  - art
  - art/WhimsyScoundrel
tagline: (empty)
created: <% tp.file.creation_date("YYYY-MM-DD, HH:mm") %>
created_date: <% tp.file.creation_date("YYYY, MM/DD") %>
created_time: <% tp.file.creation_date("HH:mm") %>
coverImage:
header:
description:
thumbnail:
dg-publish:
dg-content-classes: cards, img-grid
cssclasses:
  - cards
  - img-grid
leftAt:
characters:
---
<%*
	// Prompt for header
	let header = await tp.system.prompt('Add Header (header)');

	// Prompt for description
	let description = await tp.system.prompt('Add brief context (description)');
	
	//prompt for character tags
	let tagsInput = await tp.system.prompt('Add Character Name(s), comma-separated. (Rappy, Zu, etc; added to tags)');
	let charTags = tagsInput
		.split (',')
		.map (t=> t.trim())
		.filter(t => t.length > 0);
		
	// prompt for leftAt
	let leftAt = await tp.system.prompt('Where was it left? (diner, coffee shop, etc)');
		
	
	
	//Add values to frontmatter
	const file = tp.file.find_tfile(tp.file.path(true));
	await app.fileManager.processFrontMatter(file, (frontmatter) => {
		frontmatter.header = header;
		frontmatter.description = description;
		frontmatter.leftAt = leftAt;
		frontmatter.characters = charTags;
		//add character tags to frontmatter
		const existingTags = Array.isArray(frontmatter.tags)
			? frontmatter.tags
			: frontmatter.tags
				? [frontmatter.tags]
				: [];
		frontmatter.tags = [...new Set([...existingTags, ...charTags])];
	});	

	//Rename the file with date and header
	await tp.file.rename(tp.date.now("YYYY-MM-DD") + " - " + charTags + "- " + header);
%>
Sighted In The Wild:  


# <%- header %>



<%- description %>



> [!clue|tape-b paper-d]+ Where Was I?
> <%- leftAt %>







---