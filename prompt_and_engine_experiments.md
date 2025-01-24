# Prompt and Engine Experiments

# ChatGPT
## First Pass (demoed Jan24, 2025)

You are a trained historian editing primary sources American History.  Please mark up the entities in the following document using HTML tags.  

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers

If you see an entity of one of these types, use anchor tags to mark it up, using the title attribute to indicate the type of entity.  For example, "We bought nails from Miller's store today" could be marked up as "We bought nails from <a title="Businesses">Miller's store</a> today".

Here is the text to mark up:
[First Result](chatgpt_ner.html)

## Second Pass (demoed Jan24, 2025)

That's fantastic!  I'd like you to try something a little more complex: there is a JSON file with a list of entities which may appear in the text at https://raw.githubusercontent.com/SubjectSpotter/sample-documents/refs/heads/main/all_subjects.json.

Please read the list of entities, and consider the ID, title, description and categorization of each entity.  Then read the text and use HTML mark-up to tag each entity within the text.  Use anchor tags to surround the text mentioning an entity, adding the ID of the entity in the ID attribute of the tag, and the title of the entity in the title attribute of the tag.

Here is the text to mark up:
[Second Result](chatgpt_ner_2.html)

## Third Pass (demoed Jan24, 2025)
You are a trained historian editing primary sources from American History.  Please mark up the entities in the following document using HTML tags.  First, read this list of entities which may appear in the text: https://github.com/SubjectSpotter/sample-documents/blob/main/all_subjects.json

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers.  

If you see an entity of one of these types, look for it in the list, using the categorization and description of the entity to resolve ambiguity.  Use anchor tags to mark up the text, using the title attribute to store the entity's title from the list, and the id attribute to store the ID of the entity.  

Here is the text:
[Third Result](chatgpt_ner_3.html)



# Google Gemini
Note: Gemini cannot read links but will pretend it has, sometimes convincingly.  

I had to attach the json file.
## First Pass  (demoed Jan24, 2025)

[First Result](gemini_ner_1.html)
You are a trained historian editing primary sources from American History.  Please mark up the entities in the following document using HTML tags.  First, read the attached file all_subjects.json, which contains a list of entities you may see in the text.

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers.  

If you see an entity of one of these types, look for it in the list, using the categorization and description of the entity to resolve ambiguity.  Use anchor tags (`a` tags) to mark up the text, using the title attribute to store the entity's title from the list, and the id attribute to store the ID of the entity.  For example, `I talked to Mr. H. Hinds` would be tagged as `I talked to <a id="94795" title="Hinds, Howell">Mr. H. Hinds</a>`.

Here is the text:

## Second Pass
### System Prompt
You are a trained historian editing primary sources from American History for a digital scholarly edition.

### User Prompt
Please mark up the entities in the following document using HTML tags. First, read the attached file all_subjects.json, which contains a list of entities you may see in the text.

Here are the types of entities you may encounter: Businesses, Events, Military Units, Occupations, Organizations, People, Places, Social Identifiers.

If you see an entity of one of these types, look for it in the list, using the categorization and description of the entity to resolve ambiguity. Use anchor tags (a tags) to mark up the text, using the title attribute to store the entity’s title from the list, and the id attribute to store the ID of the entity. For example, <code>I talked to Mr. H. Hinds</code> would be tagged as <code>I talked to &lt;a id="94795" title="Hinds, Howell"&gt;Mr. H. Hinds&lt;/a&gt;</code>.

Here is the text:
<pre>
State of Mississippi
Pike County S S.

Know all men by these presents that we Stephen McClendon and Jesse Wallace & W A Barr are held and firmly bound unto the State of Mississippi in the sum of Five Thousand dollars, for which payment we bind ourselves our heirs executors administrators and assigns, each jointly and severally firmly by these presents.

Witness our hands and seals this 2nd day of June A D 1864.

The condition of the above obligation is such that whereas, the above bound Stephen McClendon has made application for the office of "Dispenser of Liquors" for Pike County. Now therefore if the said Stephen McClendon, (if appointed as Dispenser aforesaid) shall well and truly observe and strictly obey all the requirements of the law in this behalf made, and provided, and shall strictly account for, all liquors dispensed by him then the above obligation to be void otherwise to remain in full force and virtue

Stephen McClendon [seal]
Jesse Wallace [seal]
W. A. Barr [seal]

State of Mississippi
Pike County S. S.

Before me Charles Bancroft clerk of the Probate Court in & for said County personally app-eared Jesse Wallace and W. A. Barr, who being by me duly sworn say that they are worth the amount of the penalty of the above bond over and above their liabilities

Jesse Wallace
W. A. Barr

Sworn to and subscribed before me and witness my hand and the seal of said Court at Holmesville this June 2nd A D 1864

Chas Bancroft
Clerk

Pike co
application
</pre>

[Second result](gemini_ner_2.html)


# Claude
## First Pass  (demoed Jan24, 2025)
(identical prompt to Google Gemini first pass)
[First Result](claude_ner_1.html)

# GliNER
[10 Experiments with GliNER](https://docs.google.com/document/d/1pvs_5dymDEDBsvwsMza_21RHF6Szfsn_UunISwuiTNE/edit?usp=sharing)

