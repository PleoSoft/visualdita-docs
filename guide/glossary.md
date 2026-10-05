# Your glossary

[User guide](README.md) › Your glossary

Visual DITA works with the glossary your DITA project already has: its terms read on the page as the glossary writes
them, a glossary term says what it means when you point at it, you insert terms by their words, add new ones from
words you select, and every topic is checked for words the glossary says not to use.

## What your glossary is

Your glossary is the glossary entries (`<glossentry>`) your maps give keys to, as `<term keyref>` and
`<abbreviated-form keyref>` need them: a topic uses the glossary of the map it belongs to. An entry can be a file of
its own or one of several in a `<glossgroup>`, its key then naming it (`href="brakes.dita#abs"`); keys can be given
by `<glossref>` (in a glossary map of its own, as Oxygen's guide recommends) or by `<keydef>`, in any map the root
map reaches. Specialized glossary entries work as the standard ones do.

## Glossary terms on the page

- A `<term keyref>` with no text of its own reads as the glossary's term, and an `<abbreviated-form keyref>` as the
  entry's abbreviation or acronym.
- **Point at a glossary term** to see what it means: its term and the glossary's definition.
- **Insert › Glossary term…** (right-click) lists the terms of your glossary by their words, each with its definition,
  and an acronym or abbreviation as its abbreviated form. The one you pick goes in by key; with words selected, they
  become the term's own text.

## Adding a term

Select the words, right-click, **Add to Glossary…**. Visual DITA asks the term (your words, to write as the glossary
should) and what it means, then:

- writes the new entry where your glossary's entries are, as they are written (their `DOCTYPE`, their line ends),
  named after its key (`docking-station.dita`);
- gives it its key in the map that gives your glossary's entries theirs: one line after the last of them, written as
  they are (a `<glossref>` or a `<keydef>`, their other attributes such as `print="yes"` too). Nothing else of the map
  changes;
- makes your words a glossary term by that key, and offers to open the new entry.

A project with no glossary yet gets one laid out as Oxygen's guide recommends: a `glossary` folder beside the root map,
a glossary map there giving the entry its key, and a map reference to it at the end of the root map. Every change to a
map is checked against its document type first; where it would not be valid (a bookmap keeps its glossary in its back
matter), Visual DITA says so and writes nothing: give it a glossary map, and entries are added there.

## Consistent terminology

A glossary entry can say which forms of its term not to use, and why:

```xml
<glossentry id="usb-drive">
  <glossterm>USB flash drive</glossterm>
  <glossBody>
    <glossAlt>
      <glossSynonym>stick</glossSynonym>
      <glossStatus value="prohibited"/>
      <glossUsage>This is too colloquial.</glossUsage>
    </glossAlt>
  </glossBody>
</glossentry>
```

A topic that says "stick" is told so: *"stick": use "USB flash drive", as the glossary says (prohibited). This is too
colloquial.* Two fixes are offered, on the page (right-click the paragraph, or click the problem's marker in the
margin) and as quick fixes in the XML:

- **Use "USB flash drive"** writes the term in place of the word, capitalised where the word was.
- **Link the glossary term** puts a `<term keyref>` to the glossary entry in its place, where the document type allows
  one there. It reads as the glossary's term.

With Track Changes on, a fix is your tracked change.

- **Words are matched whole**, in any case, but a form in capitals (an acronym) only in capitals. Code, preformatted
  text and draft comments are left alone, and so is a form inside one you may use ("flash" in "USB flash drive").
- **What "do not use" means** is `visualDita.terminology.avoid`: by default `prohibited`, `obsolete` and `deprecated`.
  DITA leaves the values to your project.
- **The check is the `terms` authoring rule**: `visualDita.rulesOff` switches it off, as any other (see
  [Checking your content](checking.md)). The agent tools' check reports these words too.
- DITA 2.0 has no `glossStatus`, so its glossaries mark nothing to avoid.
