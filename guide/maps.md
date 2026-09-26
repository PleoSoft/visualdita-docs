# Maps

[User guide](README.md) › Maps

A map (`.ditamap`, or a `.bookmap`) opens as an outline of titles: what the publication contains, in its order.
Titles come from the topics themselves and from keys, so the outline reads like a table of contents.

![A map as an outline, with an entry selected, its keys and scope in the bar below, and its attributes in the Properties pane](images/map.png)

## Building the map

The ribbon's **Add** group adds, after the selected entry:

- **Topic…** — a reference to a topic that exists, picked from the project;
- **New topic…** — a new topic from a template, created and referenced in one go;
- **Heading** — a heading that groups entries without a topic of its own (`topichead`);
- **Key** — a key definition, for text or a target you reuse by key;
- **Map…** — another map, referenced from this one.

## Arranging it

Drag an entry to move it, with everything under it. The **Arrange** group moves the selected entry up or down,
indents it under the entry above or outdents it, and removes it. **Outline** folds and unfolds the whole tree.

## An entry

Select an entry to work on it. **Open** opens its topic beside the map; **Rename** changes its navigation title;
**Change file…** points it at another file. The bar at the bottom of the page sets its keys and key scope, and the
Properties pane shows all its attributes.

## The map's metadata

The map's own metadata — its `<topicmeta>`, a bookmap's `<bookmeta>` — is in the **Topic** pane, as **Map info**
(**Book info** for a bookmap): the map's short description, created and revised dates, authors, keywords, the product
and its version, and for a book its rights owner, copyright years, ISBN and publisher. It describes the publication as
a whole, and publishing tools pass some of it on to the topics. Each field is added where the map's document type
allows it, and is not offered where it does not. Like a topic's metadata it is not on the page: **Show on the page as
elements**, in the pane, puts it back as it is in the file.

## Relationship tables

**Rel. table ▾** adds a relationship table and edits it in place: rows of topics that link to each other when the map
is published.

## Conditions and branches

**Conditions ▾** previews the map through a condition set. An entry that publishes a branch through its own
condition set (`ditavalref`) shows it on its row, and a topic under such a branch previews through that condition
set when you open it.

## The DITA Map view

The **DITA Map** view in the Visual DITA side bar shows the map that publishes the topic you are working on, and
follows you as you open other topics; click a title to open that topic. Right-click a map in the Explorer ›
**Visual DITA** › **Show in Map Panel** to choose the map it shows. Its title bar also has the **Project Health
Report** (see [Checking your content](checking.md)).

Maps carry comments and tracked changes too: see [Review and compare](review-and-compare.md#maps).

Next: [Review and compare](review-and-compare.md).
