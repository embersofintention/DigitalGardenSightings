---
{"dg-publish":true,"permalink":"/src/site/notes/templates/add-art-entry/","tags":["art","art/IndexCard"],"dg-note-properties":{"permalink":"/templates/add-art-entry/","tags":["art","art/IndexCard"],"created":"<% tp.file.creation_date(\"YYYY, MM/DD\") %>"}}
---


<%*
	// Prompt for header
	let header = await tp.system.prompt('What will you name it? (header)');

	// Prompt for description
	let description = await tp.system.prompt('Enter single sentence description');
	
	//Add values to frontmatter
	const file = tp.file.find_tfile(tp.file.path(true));
	await app.fileManager.processFrontMatter(file, (frontmatter) => {
		frontmatter.header = header;
		frontmatter.description = description;
	});	

	//Rename the file with date and header
	await tp.file.rename(tp.date.now("YYYY-MM-DD-HHmm") + " - " + header);
%>


---
Sighted In The Wild:  

# <%- header %>
<%- description %>









---