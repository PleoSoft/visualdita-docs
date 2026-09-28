# Changelog

## Unreleased

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
