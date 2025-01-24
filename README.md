# research-notes
Research notes from prompt development and other experiments

# ChatGPT
## First Pass

You are a trained historian editing primary sources American History.  Please mark up the entities in the following document using HTML tags.  

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers

If you see an entity of one of these types, use anchor tags to mark it up, using the title attribute to indicate the type of entity.  For example, "We bought nails from Miller's store today" could be marked up as "We bought nails from <a title="Businesses">Miller's store</a> today".

Here is the text to mark up:
[First Result](chatgpt_ner.html)

## Second Pass

That's fantastic!  I'd like you to try something a little more complex: there is a JSON file with a list of entities which may appear in the text at https://raw.githubusercontent.com/SubjectSpotter/sample-documents/refs/heads/main/all_subjects.json.

Please read the list of entities, and consider the ID, title, description and categorization of each entity.  Then read the text and use HTML mark-up to tag each entity within the text.  Use anchor tags to surround the text mentioning an entity, adding the ID of the entity in the ID attribute of the tag, and the title of the entity in the title attribute of the tag.

Here is the text to mark up:
[Second Result](chatgpt_ner_2.html)

## Third Pass
You are a trained historian editing primary sources from American History.  Please mark up the entities in the following document using HTML tags.  First, read this list of entities which may appear in the text: https://github.com/SubjectSpotter/sample-documents/blob/main/all_subjects.json

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers.  

If you see an entity of one of these types, look for it in the list, using the categorization and description of the entity to resolve ambiguity.  Use anchor tags to mark up the text, using the title attribute to store the entity's title from the list, and the id attribute to store the ID of the entity.  

Here is the text:
[Third Result](chatgpt_ner_3.html)



# Google Gemini
Note: Gemini cannot read links but will pretend it has, sometimes convincingly.  

I had to attach the json file.


[First Result](gemini_ner_1.html)
You are a trained historian editing primary sources from American History.  Please mark up the entities in the following document using HTML tags.  First, read the attached file all_subjects.json, which contains a list of entities you may see in the text.

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers.  

If you see an entity of one of these types, look for it in the list, using the categorization and description of the entity to resolve ambiguity.  Use anchor tags (`a` tags) to mark up the text, using the title attribute to store the entity's title from the list, and the id attribute to store the ID of the entity.  For example, `I talked to Mr. H. Hinds` would be tagged as `I talked to <a id="94795" title="Hinds, Howell">Mr. H. Hinds</a>`.

Here is the text:


# Claude
(identical prompt to Google Gemini)
[First Result](claude_ner_1.html)


