# Writing on the page

[User guide](README.md) › Writing on the page

Visual DITA knows your document type: wherever the caret is, it offers only the elements allowed there, and the
keys do what that place expects. You write; the structure stays valid.

## Typing, Enter and getting out

- **Enter** continues what you are writing: a new paragraph, a new step, a new list item, the next definition. In an
  empty list item or step it steps out of the list, the way a second Enter does in Word. In preformatted text (code,
  screens, `<lines>`) and in a table cell, Enter is a new line.
- **Ctrl+Enter** leaves the element you are in — a note, a section, a table, a code block — and continues in a
  paragraph after it.
- **Backspace** and **Delete** in an empty element remove the element whole, instead of leaving an empty shell.
- **Tab** and **Shift+Tab** indent and outdent list items, and move between table cells. In a topic's title, Tab
  goes on to its short description.
- A topic without a short description shows a faint **Short description** line under its title: click it (or press
  Tab in the title) and type. Left empty, it goes again, and the file is not changed.

## Styles: what the caret is in

The **Styles** box on the ribbon names the element at the caret (*Paragraph*, *Step*, *Title*…). Its menu turns that
element into another one allowed there (a paragraph into a note, a paragraph into preformatted text), and inserts an
element after it, at the end of its parent, or at the caret. The breadcrumb at the bottom of the page shows the
whole chain of elements; click one to select it.

## The mini toolbar

Select some words and a small toolbar appears over them: bold, italic, underline, code, a highlight colour, clear
formatting, a link, a comment, and **Condition…** to tag the words for an audience or product.

![The mini toolbar over two selected words](images/selection-bar.png)

**Format painter** (the brush in the Font group) copies the formatting at the caret — bold, the element such as
`<uicontrol>`, the colour — onto the next words you select; double-click it to paint several times, **Esc** stops.

## Inserting elements

The ribbon's **Insert** group has the common ones: note, section, step, code block, table, link, image, equation,
reuse. Right-click › **Insert** has everything the document type allows at that spot, grouped by where it goes —
inline at the caret, after the current element, at the end of its parent — with **All elements… (Styles list)**
for the rest.

![Right-click › Insert, with the elements allowed inline, after the paragraph and at the end of the body](images/insert-menu.png)

The same right-click menu turns the element into another, deletes it (also **Ctrl+Shift+Delete**), shows where the
topic is used, makes the element reusable (gives it an id to conref), and opens the XML at that place. **Extract … to
new topic** writes a plain topic, or one of your topic's own type when its content needs it (your own elements);
**Make … reusable** moves the element into a topic you pick, and says so when that topic's document type does not
allow it there.

## Links, images and reuse

- **Link** (**Ctrl+K**) links the selected words to a topic, or to an element in it, picked from your project; keys
  work too. A link's text and target resolve on the page. With the caret on a link, a small bar shows where it goes,
  with **Open**, **Change…**, **Key…** and **Remove link**.
- **Images**: **Image** on the ribbon picks a file, or paste or drop an image onto the page — it is saved in an
  `images` folder next to the topic. Drag a corner to resize it; the size is written as DITA expresses it
  (`@width`, `@scale`, `@scalefit`).
- **Reuse** inserts content written once elsewhere, by key (`conkeyref`) or from a file (`conref`). Reused content
  shows on the page as it will be published, read-only; one click opens its source. An element reuses its own type
  or a specialization of it (a note can reuse a hazard statement, not the other way round), so the element inserted
  is the one the reused content can fill; Visual DITA says so when the reused content has elements your document
  type does not.
- **Keys**: text defined by a key (`<keyword keyref="product"/>`) shows its value, resolved through the map and its
  key scopes.
- **Renaming and moving files**: rename or move a topic, map, image or folder in the Explorer, and Visual DITA offers
  to update what points at it — the maps' entries and key definitions, links, reused content, images — and, for a
  file that changes folder, its own references. **Show Changes First** shows every file as it is and as it would be,
  before anything changes; **Always** and **Never** stop the question (the `visualDita.updateReferences` setting).
  References through keys need nothing: only the key's definition in the map changes. Only the references change:
  every other byte of each file stays as it was. A file open with unsaved changes gets the update in its editor, to
  save with the rest of your changes.
- **Renaming an id or a key**: right-click an element with an id › **Rename id…**, or an element with a `keyref` ›
  **Rename key…** (in a map, right-click the entry that defines it): every reference in the project follows —
  links and reuse by path (`file.dita#topic/element`, `#./element`), by key (`key/element`), and a key's every
  `keyref` and `conkeyref`, `scope.key` from outside its scope included. The same name in another key scope is
  another key, and is left alone. Edited as XML, **F2** does the same (see [Checking your content](checking.md)).
  A new name already taken in the topic, or in the key's scope, is refused as you type it. A subject scheme's values
  are not renamed this way: the documents' attribute values would stay behind.

![maintenance.dita renamed in the Explorer to maintaining-the-pump.dita: Visual DITA asks to update 3 references in 3 files, with Update, Show Changes First, Always and Never](images/rename-references.png)

![Show Changes First: the map and the two topics that link to the renamed topic, each as it is and as it would be, only the file name changed in each reference](images/rename-changes.png)

## Equations and drawings

MathML formulas and SVG drawings render as themselves. **Equation** inserts one inline, on its own line, or as a
numbered equation figure. Right-click a formula to write it in LaTeX, with a live preview (it is stored as MathML,
with the LaTeX kept for the next edit), or to edit the MathML itself.

## Conditions

Select words and choose **Condition…** in the mini toolbar to give them an audience, a platform or a product — or a
condition of your own document type (an attribute domain: a `@jobrole` your specialization adds). The values offered
are your subject scheme's, or the ones the project already uses. A value written the generalized way
(`props="jobrole(admin)"`) counts as `jobrole="admin"`. **Conditions ▾** on the ribbon
previews the page through a condition set (`.ditaval`) — what it excludes is greyed out — and **Show condition tags**
labels every conditional element with its values.

![With the "installer" condition set, the step for installers is greyed out and labelled](images/conditions.png)

## Attributes and the topic's metadata

The **Properties** pane shows the attributes of the element at the caret: allowed values as lists, profiling
attributes with the values in use, everything else as a text field. The topic's metadata (its `<prolog>`) is not on
the published page, so it is not on yours either: it is in the **Topic** pane — created and revised dates, authors
and keywords, the product and its version. **Show on the page as elements** puts it back on the page as it is in the
file. A map's metadata is in the same pane, as Map info (see [Maps](maps.md#the-maps-metadata)).

![The Topic pane with created and revised dates and an author](images/topic-info.png)

## Seeing the structure

- **Tags** shows every element's name on the page.
- **¶** (formatting marks) shows where each paragraph ends, which elements are empty, non-breaking spaces, and the
  authoring warnings in the margin.

## Keyboard shortcuts

| Keys | Does |
|---|---|
| Enter | a new paragraph, step or list item; a new line in preformatted text and table cells |
| Ctrl+Enter | leave the element (note, section, table…) and continue after it |
| Tab / Shift+Tab | indent or outdent a list item; next or previous table cell |
| Ctrl+B, Ctrl+I, Ctrl+U | bold, italic, underline |
| Ctrl+K | link the selection |
| Ctrl+Alt+M | comment on the selection |
| Ctrl+Shift+Delete | delete the element at the caret |
| Ctrl+Z, Ctrl+Y | undo, redo |

On a Mac, use Cmd instead of Ctrl.

Next: [Tables](tables.md).
