# Changelog

## 0.7.0

### Conditions

- **View as ▾** (the ribbon's conditions menu, under a name that says what it does) shows the page, or the map, as a
  reader gets it: through a condition set, or with the values you choose (`audience: admin`) with no condition set to
  write first: content marked for other values is left out, content marked for them or not marked at all stays;
  values of several conditions combine.
- Keys are resolved as that reader gets them: a key defined in the map for one audience and again for everyone reads
  as its readers' definition, in the text, the links and the content reused by key, and in the topics' titles a map
  shows.
- While a condition set or a view is previewed, a bar above the page says which, with **Excluded content**: **Dimmed**,
  greyed out and labelled where it is, or **Hidden**, off the page (a reader's view); either way you edit what the
  readers get, while what the view leaves out is kept as it is, its conditions too (to change it, stop previewing);
  **Open .ditaval** for a condition set, its file in its editor beside the page; **Save as .ditaval…** for a view, a
  new condition set to publish exactly what the page showed (**Open** in the confirmation opens it beside the page);
  and **✕** to stop previewing (*Viewing as audience: admin*, *Viewing through print.ditaval*). The same on a map's
  page.
- **New condition set…**, in **View as ▾** and in the Explorer's **Visual DITA** menu on a folder, makes an empty
  `.ditaval` and opens it in its editor to write its rules. **View as ▾** lists the condition sets as they are as soon
  as one is made or deleted, in VS Code or outside it.
- The condition set editor reads each rule as a sentence (*Exclude where attribute audience is admin*), offers the
  values the project uses, says what each rule does to the content, and shows a flag's colours and style on a sample;
  it fits beside a page, its rules wrapping instead of scrolling sideways.
- On a map, right-click an entry › **Condition…** sets its conditions with the same picker as on a topic.
- A topic only read (a file VS Code keeps read-only, an earlier version from Git) keeps the ribbon's View group:
  **View as ▾**, **Condition tags**, **Tags**.
- **View as ▾** is the choice alone: **All content**, the condition sets and the **Values**; a long list gets a filter
  (type part of a value, **Enter** takes the first one left).
- **View as ▾** lists each condition set by its name, with a line under it saying what it does (*platform: web only ·
  audience: not admin*), its rules in full on hover.
- The choice in **View as ▾** stays with you: each topic or map you open next opens with it, dimmed or hidden as you
  left it, until you choose another or **✕**; pages already open keep their own.
- Content with conditions is marked on the page, always and quietly: words carrying some are underlined with dots, a
  paragraph, a list item, a step, a note, a table row or any block carrying some has a bar in the page's left margin,
  all in one column, and so do the lines of words carrying some; their values show on hover. **Condition tags**,
  a button of its own in **View**, writes them beside it, the margin bar staying as it is.
- With the caret in conditioned content, a bar says what carries the conditions and their values, with **Change…** and
  **Remove** (words that were only wrapped to carry them are unwrapped).
- Right-click › **Condition** lists the elements around the pointer, innermost first, each with its values
  (*Paragraph · platform: linux*, *Section*, *Topic*), and **Selected words** first when there are some; pick one to set
  its conditions. Pointing at one outlines it on the page.
- **Condition…** on all the words of a paragraph or a phrase sets the paragraph's or the phrase's own conditions, its
  values ticked as Properties shows them, instead of wrapping its words again; on an element selected in the
  breadcrumb (a table, a section), it sets that element's; on some words, the picker says what they are inside of.
- The values offered include those the open topic uses, set in Properties and not saved yet.

### Keys

- A topic's keys come from the map you have open when that map has the topic: open a publication's map and its topics
  read with its keys, the product name and the other text it defines; with a chapter's map open, its publication's.
  Otherwise from the nearest map that publishes the topic. `visualDita.rootMap` still names one map for every topic.
- A map that refers to other publications as peers (`scope="peer"`) is a publication of its own: its topics get their
  keys from it, and the DITA Map view lists each peer publication as one entry, to open, instead of all its contents.
- A link, or reused content, by another publication's key through the key scope its peer map reference gives it
  (`admin.users`) resolves, as soon as you write it: Visual DITA reads that publication's keys the first time a topic
  uses one, and the link opens its topic there.
- A link's **Key…** offers the other publications your map refers to as peers, one entry each (`admin.…`); choose
  one for its keys.
- **Where used**, and **Referencing** in DITA References, list the topics of other publications that link to a topic
  through its key scope, and answer at once in a large documentation set.
- Check References, the Explorer's marks and the Project Health Report check a key where its topic reads it, as its
  page does: a key defined only in another publication, or another release, is a key no map defines for it; a key of
  another publication through its key scope is defined. The Project Health Report also lists the key definitions
  nothing uses.
- The DITA Map view folds a map's key definitions into one **Keys** row, with how many there are, so that hundreds of
  them no longer push its table of contents out of sight; **Filter** finds them there too.

### Large projects

- In a large documentation set a topic opens with its keys at once, the first one of a window too: the maps a topic is
  read in are read once, and again when one of them changes; the DITA Map view reads a publication's entries when you
  expand it, or open one of its topics, instead of every publication's at once, and finds the publication of the topic
  you open among hundreds; the keys of a big publication, and the titles of its map, are there at once; opened again,
  the publications are not looked for again.
- A large documentation set is read about four times faster the first time, and opened again, Visual DITA finds
  what changed in a second instead of seconds: DITA Search, Check References and the Explorer's marks are ready
  sooner.
- **View as ▾** offers the values every topic and map of the project uses, and every subject scheme's, however large
  the project; it looked at the first 5,000 topics and 200 maps only.
- The Explorer's marks are worked out again in about a second after a change in a large documentation set, where
  publications refer to each other as peers, instead of several seconds.
- **Publish…** and **Publish Map…** on a topic find the maps that hold it at once in a large documentation set; a
  topic published alone takes its keys from the map it is read in, as its page does.

### Fixed

- A map that is part of a publication (a chapter's own map) is published with the keys of the publication, as its
  topics read in Visual DITA; it was published without them, its product names and other key text empty.
- In the DITA Map view, the rocket in the title bar publishes the map shown, whichever row is selected, instead of
  the selected topic alone.
- The DITA Map view listing several maps titles each map's topics with that map's own keys (a product name of one
  release in that release's map), instead of the first map's.
- The Project Health Report counts a map's own topics: another publication it refers to as a peer (`scope="peer"`)
  is counted with its own map, not added to this one.
- A link brought back by undo shows its title, and whether its target is there, at once, instead of after the page
  was opened again.
- **Condition…** on selected words: a value typed and not yet confirmed with **Enter** is applied with **Apply**,
  instead of being dropped; the words then show their condition, and the status line says what was set.
- **Properties** of a map entry offers the condition values to tick (audience, platform, product…), as on a topic.
- With a condition set (`.ditaval`) in front, **Properties**, **Review** and **Topic** are empty and say why, instead
  of showing the topic behind it, which a change there would have gone to.

### Images

- An image, a video or a sound chosen from outside the project is copied into it before it is inserted: Visual DITA
  asks first, then copies it into `images/` (videos and sounds into `media/`) next to the topic and inserts the copy.
  Outside the project it could not be shown on the page, and no one else, nor a publication made elsewhere, would
  find it.

## 0.6.1

### Images

- **Fit to page** in the image's bar makes an image as wide as the page (`scalefit="yes"`); pressed again, its
  natural size.

### Fixed

- Several images in a figure sit side by side on the page, as DITA places them and as they are published, instead of
  one below the other; an image with `placement="break"`, an alignment or fitted to the page keeps a line of its own.
- A percentage typed in an image's **Width** (`50%`) is written as DITA's `scale="50"`, a percentage of its natural
  size, instead of a width DITA does not take; a size typed there replaces the scale or the fit it contradicts.

## 0.6.0

### DITA Search

- **DITA Search**, at the top of the Visual DITA side bar (**Ctrl+Alt+F**, **Visual DITA: Search DITA…**), searches
  the text of your topics and maps as a reader reads it, never the markup, as you type: every word (a word also finds
  the longer words it begins), with or without capitals and accents, a "phrase in quotes" exactly; titles first. A
  misspelt word that finds nothing is searched as the nearest word your project uses, and said. What it finds is
  grouped by topic, each place said for what it is (a title, a step, a note) with the words found marked; a click
  opens the topic with the caret there.
- Keep it to a kind of element (titles, notes, steps, tables, code and more; your specializations count); when the
  DITA Map view shows one map alone, it keeps to that map's topics, and says so, with **Show all maps**.
- Nothing to wait for or refresh: what you type is found before you save, and files changed outside VS Code (a Git
  pull or branch switch, a folder renamed or deleted, even while VS Code was closed) are found too. Nothing is added to
  your project, and a large project stays fast. Files over 5 MB are not searched.
- **Visual DITA: Rebuild Project Index** (also in the DITA Search view's **…** menu) reads your whole project again.
- Agents search the same way: the agent tool `dita_search` finds your project's text as DITA Search does (words or a
  phrase, a kind of element, a map).
- **Where Is This File Used**, the DITA References view, **Go to Symbol in Workspace** (**Ctrl+T**), the Explorer's
  marks, the **Project Health Report** and **Check References** answer at once, from what DITA Search knows of your
  project, instead of reading every file each time; the marks, the report and the check follow what you write, before
  you save. The report counts topics in DITA `.xml` files too, as the marks do.

### Your Schematron rules

- Your project's own checks, written in Schematron, run as you write, beside the grammar and the authoring rules:
  the rules a topic or map names in its `<?xml-model?>` (as Oxygen writes it), and those `visualDita.schematron`
  lists. Their findings show on the page, in the XML and in the Problems panel, each rule's `severity` or `role` its severity, and
  on the page each names the rules file it comes from.
  Rules for XSLT 2 and 3 work as they are: their own functions and keys, the XSLT libraries and Schematron files they
  include, abstract patterns, and the files they open, read from where the document is. DITA's classes come from your
  document type.
- **Check the Project Against Its Schematron Rules** checks every topic and map your rules apply to, open or not,
  each finding in the Problems panel.
- The **DITA Document Types** view lists your rules files and the phase each checks with: its default phase, or another
  you choose with **Choose Phase…** (one of its phases, or every pattern), kept in `visualDita.schematronPhases`.
- The agent tools' check (`dita_check_topic`) reports your Schematron rules' findings too, with the phase chosen, each
  with the fixes Visual DITA offers for it.
- The fixes your rules give their findings (Schematron QuickFix) are offered on a topic's page, from the right-click menu
  and the problem's marker in the margin, and as quick fixes in the XML. A fix that asks for a value asks first; it
  changes only what it names, the rest of the file as it was; with Track Changes on, it is your tracked change.

### Your terminology

- Each topic is checked against your DITA glossary: a word a glossary entry says not to use (its `glossStatus`, such
  as `prohibited`) is pointed out with the term to use and the glossary's reason, on the page, in the XML and in the
  Problems panel. Your glossary is the glossary entries your maps give keys to; `visualDita.terminology.avoid` says
  which statuses mean "do not use". It is the `terms` authoring rule. Entries grouped in a `<glossgroup>` count as
  entries in files of their own do, and a `<term>` or `<abbreviated-form>` whose key names one reads as its term on
  the page.
- Two fixes, on the page and as quick fixes in the XML: **Use "…"** writes the term in place of the word, and **Link
  the glossary term** puts a `<term keyref>` to the glossary entry there. With Track Changes on, a fix is your tracked
  change.
- The agent tools' check (`dita_check_topic`) reports these words too.
- **Insert › Glossary term…** (right-click) lists your glossary's terms by their words, each with its definition, an
  acronym or abbreviation as its abbreviated form; the one picked goes in by key (`<term keyref>`,
  `<abbreviated-form keyref>`), the words selected becoming its text. A glossary term on the page says on hover what
  it means.
- **Add to Glossary…** (right-click on words you select) makes them a new glossary entry, the term and its definition
  asked: written where your glossary's entries are, as they are, its key one line in the map that keys them, written
  as those keys are (`<glossref>` or `<keydef>`); your words become a term by it. A project with no glossary yet gets a
  `glossary` folder beside the root map and a glossary map referenced from it. A map that would not stay valid is
  left alone, and said.
- The user guide has a page of its own for your glossary.

### Publishing

- **Publish…** (right-click a map or a topic in the Explorer, **Visual DITA ›**; the rocket at the top of the editor)
  publishes it with the DITA-OT on your machine (4 or later): a map, or a topic alone with its map's keys; on a topic,
  **Publish Map…** publishes the map it belongs to. As HTML5 or PDF, both with Visual DITA's look (the PDF through a
  DITA-OT theme: fonts, headings, notes, code, tables, task sections), with the conditions of one of your DITAVAL
  files. What DITA-OT says is in the Problems panel and on the page; without DITA-OT or Java, Visual DITA says what to
  get.
- What you publish can be kept in the project, as DITA-OT's own project file (`publishing/project.xml`) with the
  stylesheet and the PDF themes beside it (`theme.yaml`, yours, over Visual DITA's): `dita --project=publishing/project.xml`
  publishes your maps the same way on a server.
- A project already set up for DITA-OT is published as it is: **Publish…** offers the deliverables of your own DITA-OT
  project files (XML, JSON) and publishes them as written, and any output type your DITA-OT has (its plugins' among
  them).
- DITA-OT's parameters are settings (`visualDita.publishing.html5`, `.pdf`), Visual DITA's look one too
  (`visualDita.publishing.look`); HTML5 by default as help pages are, the map's contents beside every topic.
- DITA-OT publishes the files as saved: when topics, maps or DITAVAL files have unsaved changes, Visual DITA asks
  first, **Save and Publish** or **Publish Saved Versions**.

### Published HTML with the page's look

- **Write Publishing Stylesheet…** writes a stylesheet for DITA-OT's HTML5 output with the look your topics have on
  the page: titles, notes, lists, task steps and their names, code, tables, figures, links, the colours and capitals
  a converted Word document keeps, and the numbers of numbered chapters and clauses, from your maps.
- It offers the DITA-OT arguments that use it, and with DitaCraft installed, puts them in its settings for this
  workspace.

### The page

- A video, a sound or an embedded page (`<object>`) shows on the page as a card saying what it is and where it is,
  and plays there: a sound or video file of your project in place, one from a web server once you allow that server
  (as for images), another site's player (YouTube's) in the browser, with **Open in browser**. Click its card for a
  small bar that edits it: its address, **Replace…** with another video or sound of your project, what it plays
  (video, sound, embedded page), its width and height, **Delete**; a double-click puts you in the address.
- A related link without text of its own shows the title of the topic it names, else where it points.
- Enter where no paragraph may follow makes what your document type allows next, the same kind first: the next
  author in the prolog; where several things may follow, a menu at the caret offers them.
- A related link is edited on the page: a click selects it (its link bar: Open, Change…, Key…, Remove link), typing
  gives it text of its own, and **Insert → Related link…** adds one to a topic that has none yet. Enter works as in a
  list: a new link right after, then its target asked; Enter on a link without a target leaves the related links,
  back to the body. A link with no target shows as *Link without a target*.

### The DITA Map view

- With several root maps the view lists them all; once it shows one map (opened, or chosen), **Show All Maps** in its
  title bar, or the first entry of **Choose Map…**, lists them all again.
- **Publish…** on each row: the rocket on a map's row publishes that map, on a topic's row that topic alone, with the
  keys of the map it is listed in. The rocket in the view's title bar is there when it shows one map, and publishes it.
- Its title bar keeps **Filter**, **Show All Maps**, **Choose Map…** and **Publish…**, so the map's name has room;
  **Edit Map**, the **Project Health Report** and **Refresh** are in its **…** menu.
- **Filter** (the funnel in its title bar) finds a map or a topic by its title as you type, the others hidden;
  **Ctrl+Alt+F** in the view opens VS Code's own find there (everywhere else it opens DITA Search).

### Beside Red Hat XML

- When Red Hat XML reports problems in a DITA file (it does not know Visual DITA's grammars), Visual DITA offers once
  to stop its checks on DITA files, in your own settings (`xml.validation.filters`): it goes on checking your other
  XML, its own filters kept.

### Your framework's templates and styling

- The DITA Document Types view shows the framework in use under **Templates and styling**: the template folders and
  the stylesheets, each a click away, a setting that names nothing, and buttons to turn the styling off and on or
  take another framework.
- **Use Framework Templates and CSS…** takes from an Oxygen framework the stylesheets its `.framework` or `.exf` file
  uses, not every CSS file in its folders: its alternate and print styles, and what it takes from Oxygen's own
  frameworks, are left out. Oxygen's own frameworks give their templates, not their CSS: Visual DITA styles standard
  DITA itself.
- Author CSS with `:not(…)` applies: its selectors are rewritten for the page like the rest; so do the header cells of
  a table styled through `thead` (`*[class~="topic/thead"] *[class~="topic/entry"]`).

### Word documents converted to DITA

- **Import Word Document…** (right-click a folder in the Explorer › Visual DITA) makes a map and its topics from the
  Word documents you pick, each in a new folder there; **Convert Word Document to DITA…** (right-click a `.docx`) in a
  folder beside it. It asks where the topics start, showing how many topics each choice gives: at each Heading 1, each
  Heading 1 and 2, and so on down to every heading, nested in the map as the document is. It proposes your last
  choice, else the document's own (`visualDita.wordConversion.split` sets it until then). Each topic is named after
  its title; a heading over a numbered list a task with its steps, "Before you begin" its prerequisites; the images
  written beside. Nothing is written over. What did not come across (text boxes, drawings, fields) is said.
- Word's numbered chapters and clauses become what DITA numbers, with no number typed in: a numbered heading a
  numbered entry of the map, a clause a numbered section, a deeper clause an item of a legal list. When counting would
  not give Word's numbers, they are kept as text, as Word shows them, and that is said
  (`visualDita.wordConversion.numbers` to keep them as text always, or leave them out). A list stays one list: a
  paragraph that goes on an item is in that item, a sublist nested in its item, a list Word starts again a new one.
- Lines lined up with tabs become a table when everything says they are one: the same tab stops on every line, a bold
  header row or a column of codes and figures ("$400", "3 days"), no list labels. Its header lines are joined, the
  centred lines above it its title, a line broken by hand in a cell one line, columns Word laid side by side read one
  after the other, and what every page repeats (the title, the column headings) is kept once.
- A document whose own styles are its headings (a style with an outline level, or a bold one used only for short
  lines) has those as its headings, a heading on two lines one, put in a sentence's case when typed in capitals.
  A document without heading styles: its short bold lines are its headings, the bigger the higher. The map is titled
  by the running title of the page footer or header when the document has no Title, and carries the copyright they
  state.
- A form typed without Word's lists: numbers typed before a tab ("1.", "a.") become lists, nested by how far they are
  indented, a paragraph indented with an item going on with it. Its first lines centred and bold title the map; the
  lines typed above them, a "Page 1 of 2", and at its end a copyright or a line repeating the header are left out,
  the copyright the map's. A list of definitions ("Boat" means…) or of titled clauses stays a concept, not a task.
- What DITA keeps of the look comes across: text colour, shading and capitals as outputclass, shown on the page;
  Word's highlighter as the page's highlight; a centred or right-aligned paragraph's alignment; an image's size and
  placement; a table cell's shading and alignment. Hidden text and a form field's placeholder ("Click or tap here to
  enter text.") are left out. What was read from the look is said.
- Word's equations become equations (MathML), as **Equation** inserts them, to be edited on the page; one on a line
  of its own an equation block, one in a sentence an inline equation.
- A drawing that is not a picture (a shape, a chart, SmartArt) is marked where it was, named, as DITA's
  `required-cleanup`, for a picture of it to take its place; a text box's words come across as text. A picture in
  EMF or WMF, which browsers and most PDF output do not show, is said.

### Numbered chapters and clauses

- The page shows the numbers publishing gives: a map's entries marked numbered (`outputclass="numbered"`) on the map
  and before their topic's title, a topic's numbered sections after it (`6.1`, `6.2`), the items of a legal list
  (`outputclass="legal"`) after their section's (`6.2.1`). Nothing is typed in: a section added beside numbered ones
  is numbered, and the ones after it renumber.

### Extract to new topic, like a refactoring

- Select paragraphs, lists, tables or a whole section and right-click › **Extract selection to new topic…**: the new
  topic asks for its title, offering the first line.
- The new topic goes into every map that uses the topic, under it, and links and reuse that pointed into what moved,
  in this topic and in the others, point at the new topic; a link to an extracted section opens its topic. Its own
  links back still point where they did. With a map to hold it, nothing is left in its place.
- A nested topic is extracted whole: its short description, its prolog and the topics nested in it go with it, its id
  kept, and links into any of them follow it to the new file.
- The reverse: right-click an entry in the map › **Inline into parent topic…** moves its topic into the topic of the
  entry it sits under, as a section (when it is that simple: its title the section's, its number kept) or as a nested
  topic, whole. Its entry leaves the map, its own entries take its place, every link and reuse follows it, and its
  file goes.
- A section extracted to a new topic gives the topic its id, so a section extracted and inlined again is as it was,
  its id and the links to it included.

### Pasting a Word document

- A Word document pasted on the page comes in as DITA: pasted in an empty paragraph, its headings become sections
  titled by them where the body takes sections (within a paragraph's text, bold paragraphs); "Note:", "Caution:" and
  the like become notes of that type, a list nested in Word stays nested, and pasted into a new, empty topic it gives
  the topic its title.
- Its images are saved in an `images` folder beside the topic; a caption makes the image a figure, or a table's
  title, without Word's "Figure 1:". Footnotes become DITA footnotes where they are referenced, Quote paragraphs long
  quotes, lines in a code font a code block.
- What Word shows but is not content stays out: its table of contents (publishing makes one), the numbers of numbered
  headings and lists, and text deleted with Track Changes on (its insertions are kept, as if accepted).

### Images from a web server, on your word

- An image in a topic from a web server no longer loads by itself: loading it tells that server the topic was opened.
  A line above the page names the server, with **Load This Time**, **Always from …** and **Never**; until then the
  image is a placeholder that says where it comes from. Always and never are kept in your own settings
  (`visualDita.remoteImagesAllowed`, `visualDita.remoteImagesBlocked`), which a project cannot set; the page is only
  allowed to load from the servers you allowed. `visualDita.remoteImages` (ask, show, never) decides for the others.
- What the page is not allowed to load is refused and noted in the status bar, with the details in the Visual DITA
  output.

### Fixed

- A topic or a map opens without waiting for the conditions used across the project to be counted, seconds in a big
  project: they come a moment later. Saving a map counts them once for all the open pages, not once each. A page that
  takes longer says "Opening…".
- A list copied from Word pastes as one list, numbered through, not as a list per item.
- Strikethrough pasted from Word or a web page is kept; so are text colour, capitals, the highlighter and a centred
  or right-aligned paragraph, as the Word import keeps them. A web page's black and grey text stays plain.
- A topic's title reads without its footnotes and index terms where it is shown elsewhere: in maps, the DITA Map view
  and links to it.
- A map changed outside the page (by an assistant, a conversion, Git) shows the titles of the entries it gained.
- A topic being edited keeps its edits when a map changes (a key added, an entry moved, in another tab or by an
  assistant): it went back to how it was when opened, while the file kept the edits, and the next edit wrote the old
  text back.
- After **Rename key…**, a topic open on the page has the key by its new name at once: a link or reuse by that key
  resolves without reopening the page.
- A link to a file whose name has a space or an accented letter in it (`my%20topic.dita`) shows the topic's title and
  opens, on the page and in the map, instead of looking broken.
- A link by key (`<xref keyref>`, `<link keyref>`) shows the title of the topic or element the key names, when the
  map gives the key no text of its own, and **Open** follows it.
- **Open** on a link to an element in a topic opens the topic with the caret in that element; a link within the same
  topic moves the caret there.
- Reused content shows what its source says of itself where the reusing element says nothing: a reused
  `<note type="caution">` reads as a Caution.
- A Markdown topic (`format="markdown"`), or HTML, a PDF or an image, that a map entry or a link points at opens in
  the editor VS Code has for it, not in Visual DITA: from the map, the DITA Map view, a link on the page and the DITA
  References view.
- A menu cascade reads as part of its sentence, **File › Save as**, instead of putting each control on a line of its
  own. The spacing between the controls in the file is kept as it was, even when one of them is edited.
- Right-click a key's text on the page (a keyword whose text the key gives) or a link that shows its target's title,
  and the menu is that element's, with **Rename key…** for a key. In a table the menu is for what the pointer was on,
  not the line above it once the table bar has appeared.
- A second Enter in an empty step leaves the steps, the empty step going, also when the task already has a result:
  the caret goes to the start of the result, instead of a new step at each Enter.
- **Where Is This Used** and the DITA References view find a topic reused through keys from another map, or another
  repository of the workspace, and no longer count a key of the same name that means another topic there.

## 0.5.0

### Writing a map as an outline

- A map can be typed before its topics exist: **Enter** in the map's title starts it with a heading, **Enter** at
  the end of a heading's title adds the next one, **Tab** and **Shift+Tab** nest it while you type, **Escape** leaves
  the title.
- **Create topic…** (the Entry group, or right-click) makes the topic of an entry that has none, from a template,
  titled as the entry; right-click › **Create topics for the … entries without a file…** makes them all from one
  template. The entry becomes the reference to its topic.
- New topics, from **New topic…** too, go into the folder of the topics around them in the map, not beside the map.
- **Topic…** and **Map…** take several files at once: they are added one after the other, in name order.

### Maps of your own document type

- **More ▾** in the map's Add group, and right-click › **Add**, offer the other entries your map's document type
  allows where the entry goes: a group, and your own entry types, a term map's term groups for instance. An entry
  that references a file asks for it; a group that must hold an entry asks for its first one.

## 0.3.0

### Rename ids and keys, and find where they are used

- **Rename id…** (right-click an element with an id) and **Rename key…** (an element with a `keyref`, or a map entry
  that defines the key) rename it and every reference in the project: links and reuse by path
  (`file.dita#topic/element`, `#./element`) or by key (`key/element`), and every `keyref` and `conkeyref`,
  `scope.key` from outside its scope included; the same name in another key scope is left alone. The files that had
  no unsaved changes are saved. Edited as XML, **F2** does the same, and **Ctrl+Enter** shows every change first.
- **Shift+F12**, edited as XML, lists every place an id or a key is used.
- The Explorer marks topics and maps: how many references do not resolve, `!` for a document type not licensed, a
  topic no map uses greyed (`visualDita.explorerBadges`).
- **Go to Symbol in Workspace** (**Ctrl+T**) finds a topic, section, figure or table by its title, a map, a key, or
  an id (`#id`).
- Edited as XML, a topic or map has its **Outline**, breadcrumbs and sticky scroll: topics, sections, figures and
  tables by their titles; a map's entries, headings and key definitions.

### Your own document types: conditions, reuse, and topics not licensed

- Conditions of your own document type — an attribute domain such as `@jobrole` — work as `@audience` does: in
  **Condition…**, in Properties with your subject scheme's values, previewed and flagged through a condition set,
  tagged on the page, checked against the subject scheme, and offered in the condition set editor. A value in the
  generalized form (`props="jobrole(admin)"`) counts as `jobrole="admin"`.
- Reuse: a conref or conkeyref pulling an element of another type (a paragraph reusing a step), or content with
  elements your document type does not have, is said (the `reuse` rule). **Reuse** inserts an element the reused
  content can fill, its own type or one it specializes, never the other way round.
- **Extract … to new topic** writes a topic of your topic's own type when the plain topic cannot hold the content;
  **Make … reusable** refuses a topic whose document type does not allow the element, and leaves that topic's
  unsaved changes as they are.
- A topic of your own type that is not licensed — its root element is yours, a `<warranty>` — opens read-only instead
  of as a single tag: your elements as labelled boxes around their content, the DITA inside them as usual, the status
  line naming each element. The banner says why; the XML stays yours to edit.

### Your document types in RELAX NG

- Specializations and constraints written as RELAX NG shells (DITA 1.3 and 2.0, the XML syntax) come as a Visual
  DITA package, as DTD-based ones do: their topics open on their own grammar, named by the `<?xml-model?>` at their
  top, with their elements on the page, in the menus and in the check.

### Fixed

- **Conditions ▾** and, in a map, **Rel. table ▾** open wherever they are clicked: on their icon or their label, the
  menu closed again at once.
- Check References no longer reports `#./element` (the topic a reference is in, DITA 1.3) as a missing topic ".".
- **Open Map Source at Entry** and **Open Source at Line** are no longer offered in the Command Palette, where they
  failed: they open the entry or line they are chosen on, from the view's right-click menu.
- A topic naming a standard OASIS RELAX NG or XML Schema shell (`urn:oasis:names:tc:dita:rng:concept.rng`) opens on
  standard DITA, not on a shell of the same file name in one of your packages. Two packages that each have a shell of
  the same name (two `topic.rng`) each get the topics that name theirs, by URN or by path.
- The DITA Document Types view shows a package of RELAX NG document types licensed, as the topics are, and names its
  document types without `.rng`.

## 0.2.0

### Link management ([#1](https://github.com/PleoSoft/visualdita-docs/issues/1))

- **Rename or move a topic, map, image or folder** in the Explorer, and Visual DITA offers to update what points at
  it: the maps' entries and key definitions, links, reused content and images, and, for a file that changes folder,
  its own references. **Show Changes First** shows every file as it is and as it would be; **Always** and **Never**
  stop the question (`visualDita.updateReferences`). Only the references change: every other byte of each file stays
  as it was. A file open with unsaved changes gets the update in its editor, to save with the rest.
- **Check References**, the checklist button of the DITA References view, lists what does not resolve in the topic or
  map you are on, and **Check References in the Whole Project** in the whole project: a file or image that is not
  there, an id a link or conref names that is not in its file, a key no map defines, a link to a topic no map
  publishes. Each opens the source at its line; the count shows on the view.
- Files renamed, moved or deleted outside VS Code (by Git, or another program) show at once: the DITA Map view marks
  an entry whose file is not there, the topics linking to it show the problem, the page shows a missing image as
  missing, and a check listed in the DITA References view runs again.
- The DITA References view stays with a topic or map open as XML, topics saved as `.xml` included, and shows in any
  project with maps, as the DITA Map view does.

### Fixed

- Properties: an attribute with many values from the subject scheme (audience, platform, product…) lists them in even
  columns under its name, each checkbox beside its value, instead of a ragged wrap; a click on the name no longer
  ticks the first value. ([#2](https://github.com/PleoSoft/visualdita-docs/issues/2))

## 0.1.0

First public beta. What it does is described in the [README](README.md), and reviewing and comparing in
[Review and compare](guide/review-and-compare.md).
