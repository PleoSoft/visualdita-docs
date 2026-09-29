# Changelog

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
