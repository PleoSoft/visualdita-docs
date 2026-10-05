# Checking your content

[User guide](README.md) › Checking your content

Visual DITA checks each topic while you write, against its document type (the grammar: which elements go where,
which attributes and values are allowed), a set of authoring rules (what a good topic has, beyond what the grammar
requires), and your project's own rules when it has them in Schematron.

![A topic with problems: markers in the margin, a broken link underlined, an empty paragraph labelled, the count in the status line, and the list in the Problems panel](images/problems.png)

## Where problems show

- **On the page**, on the element they belong to: errors underlined in red; with the formatting marks (**¶**) on,
  a marker in the margin for each problem, warnings and notes included.
- **In the page's status line**: how many problems the topic has. Click it to go to the next one.
- **In VS Code's Problems panel** (**Ctrl+Shift+M**): every problem with its line, for the topics you have open —
  as a page or as XML.

## The grammar

The check follows the topic's own document type — standard DITA, or your licensed package — exactly: elements, their
order, attributes and their values. A topic whose document type Visual DITA does not have is not checked against a
stand-in, because every element of your own would be reported (see [Your document types](document-types.md)).
`visualDita.validation` switches the grammar check off.

## The authoring rules

Beyond the grammar, the rules point out:

| Rule | Points out |
|---|---|
| `shortdesc` | a topic without a short description, or with one over 50 words. On the page, a faint **Short description** line under the title adds one (click it, or press Tab in the title); in the XML, the quick fix **Add a short description** does |
| `empty` | an empty title, paragraph, list item, note or section |
| `keys` | a key no map defines |
| `files` | a link or reference to a file that is not there |
| `reuse` | a conref or conkeyref that pulls an element of another type (a paragraph reusing a step: an element reuses its own type or a specialization of it), or content with elements your document type does not have |
| `subject-scheme` | a profiling value your subject scheme does not allow |
| `alt` | an image without alternative text |
| `ids` | an id used twice in a topic |
| `external-scope` | a link to a web address without `scope="external"` |
| `draft` | draft comments and required-cleanup, which the output leaves out |
| `table` | a table row with the wrong number of cells |
| `tracked` | tracked changes left in a file when the project does not track changes |
| `terms` | a word your glossary says not to use, with the term to use instead (see [Consistent terminology](glossary.md#consistent-terminology)) |

Switch any of them off for a project with `visualDita.rulesOff`, for example
`"visualDita.rulesOff": ["shortdesc", "draft"]`.

## Your terminology

A project with a DITA glossary is checked for words its glossary entries say not to use, with the term to use
instead and two fixes: see [Consistent terminology](glossary.md#consistent-terminology).

## Your own rules (Schematron)

A project with its own checks written in Schematron (an Oxygen framework's, or your team's `.sch` files) gets them
checked as you write, beside the grammar and the authoring rules. A topic or map is checked against:

- the rules its own `<?xml-model?>` names, as Oxygen writes it:
  `<?xml-model href="rules/house.sch" type="application/xml" schematypens="http://purl.oclc.org/dsdl/schematron"?>`;
- the rules `visualDita.schematron` lists for the project, relative to the workspace folder:
  `"visualDita.schematron": ["rules/house.sch"]`.

Their findings show where the others do: on the page, in the XML and in the Problems panel, as **Visual DITA
Schematron** with the rules file's name and the pattern's id. On the page, a finding's message ends with the rules
file's name, so you know the rule is your team's, not Visual DITA's. A rule's `severity` (ISO Schematron 2025), or else
its `role`, is the finding's severity: `error` or `fatal` an error, `warning` a warning, `info` a note; an assert with
neither is an error. Rules are ISO Schematron, of any edition; Schematron 1.5 rules, from before ISO, are said as such
in the Visual DITA output, to be moved to ISO Schematron's namespace. Rules test DITA by its
classes, as usual (`contains(@class, ' topic/p ')`): the classes come from your document type, as in Oxygen. Rules
written for XSLT 2 or 3 (`queryBinding="xslt2"` or `"xslt3"`) work as they are: their own XSLT functions and keys, the
XSLT libraries and Schematron files they include, abstract patterns, and the files they open (the topics a link
names, read from where the document is).

A rules file is prepared the first time a document uses it, and again when it or a file it includes changes: a second
or so, said in the status line. After that a document is checked in milliseconds, while you type. Rules that cannot be
prepared are said once, the reason in the Visual DITA output.

**Visual DITA: Check the Project Against Its Schematron Rules** (Command Palette) checks every topic and map of the
project its rules apply to, open or not, and says how many findings each rules file made; **Show Problems** lists
them, file by file, each a click away. A file closed afterwards keeps its findings, as it is on disk. Their fixes are
offered once the file is open.

### Your rules files and their phases

The **DITA Document Types** view lists your rules files under **Schematron rules**: each one with the phase it checks
with and what uses it (`visualDita.schematron`, or how many documents name it). Click one to open it; hover it for its
phases. The checklist button on **Schematron rules** checks the whole project.

A rules file with phases (`sch:phase`) checks with its default phase (`defaultPhase`), or with every pattern when it
names none. **Choose Phase…** (the filter button on a rules file, or its right-click menu) picks another: one of its
phases, each with its patterns, or every pattern. The choice is kept for the project in `visualDita.schematronPhases`,
the rules file relative to the workspace folder (`#ALL` for every pattern):
`"visualDita.schematronPhases": { "rules/house.sch": "full" }`. Every check uses it: as you write and the whole
project's. A phase the rules file does not have is said in the Visual DITA output, and that file checks nothing until
you choose one it has.

### Fixes

Where your rules give a finding fixes (Schematron QuickFix, `sqf:fix`), Visual DITA offers them:

- on a topic's page: right-click the marked element, or click the problem's marker in the margin; the fixes are at
  the top of the menu, under what the finding says;
- in the XML: as quick fixes on the finding (the light bulb, or Ctrl+.), the rules' default fix marked preferred.

A fix that asks for something (a user entry) ends with an ellipsis: choose it and Visual DITA asks, the rules' default
filled in, before making it. A fix changes only what it names: an attribute added after the others, the words a fix
replaces where they are written, the content it copies kept exactly as the file has it, its comments and entities
too. Undo takes it back. With Track Changes on, a fix is your tracked change, to accept or reject as any other. Fixes follow the Schematron QuickFix specification: adding, deleting and replacing elements,
attributes and text, replacing words in a text, generic fixes (one for each value), groups, the schema's own fixes,
fixes calling others, and parameters of an abstract pattern the fix declares.

## The whole project

**Visual DITA: Project Health Report** (Command Palette, or the DITA Map view's **…** menu) looks at the whole
doc set: each map's size in topics and words, links to files that are not there, keys no map defines, topics no map
publishes, and images nobody uses; topics in DITA `.xml` files count too. Every file is a link that opens it. It is
there at once, from what DITA Search already knows of your project, and counts what you have written but not yet
saved.

![The Project Health Report: 7 topics in one map, one broken link and one topic in no map](images/project-health.png)

**Check References**, the checklist button of the **DITA References** view, lists at the top of the view what does
not resolve in the topic or map you are on: a file or image that is not there, an id a link or conref names that is
not in its file, a key no map defines, a conref that names no element, and a link to a topic no map publishes (it
goes nowhere once published). Each opens the source at its line; the count shows on the view. **Check References in
the Whole Project**, in the view's menu, does the same for every topic and map, at once: both come from the reading of
your project that DITA Search keeps, with what you have written but not yet saved. Links to web addresses, and those
marked `scope="peer"` (another doc set), are left alone. A file renamed, moved or deleted outside VS Code (by Git, or
another program) shows at once: the DITA Map view marks its entry as not there, the topics linking to it show the
problem, and a check listed in the view runs again.

![Check References in the Whole Project: 2 problems at the top of the DITA References view, a link to a file that is not there and a link to an id that is not in its file, each with its file and line, and the count on the Visual DITA icon](images/check-references.png)

**Visual DITA: Check Grammars in Workspace** asks one more question of the whole doc set: which document types its
files declare, and whether each one resolves to standard DITA or to a licensed package. Run it when a doc set arrives,
before anyone concludes their own elements are not supported.

## When you edit the XML

With a topic open as XML (**Open Source**), the same checks run, and Visual DITA completes the elements allowed where
you type, their attributes and their values. Ctrl+click on a `keyref`, `conref` or `href` goes to its target, and
hovering one shows what it resolves to.

- **F2** on an id, a key, or a reference to one renames it and every reference in the project; **Ctrl+Enter** in
  the rename box shows every change first.
- **Shift+F12** lists every place an id or a key is used, the key/element and `#./element` forms included.
- The **Outline**, the breadcrumbs and sticky scroll follow the file's structure: topics, sections, figures and
  tables by their titles; a map's entries, headings and key definitions.

## In the Explorer, and anywhere

The Explorer marks each topic and map: how many of its references do not resolve (what **Check References** lists),
**!** for a document type no Visual DITA package licenses, and a topic no map uses greyed. Hover one to read why.
They come from what DITA Search knows of your project ([Searching your content](search.md)), so they follow what you
write, before you save, and files changed outside VS Code; `visualDita.explorerBadges` turns the marks off.

**Go to Symbol in Workspace** (**Ctrl+T**) finds a topic, section, figure or table by its title, a map by its title,
a key, or an id (type `#` and the id) anywhere in the project.

Next: [Your document types](document-types.md).
