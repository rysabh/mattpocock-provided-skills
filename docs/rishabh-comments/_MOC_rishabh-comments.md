---
name: _MOC_rishabh-comments
description:
tags:
rating:
related_notes:
  - ""
---

---
```dataview
TABLE WITHOUT ID
  join(default(rating, "—")) AS "Rating",
  file.link AS "Incoming Links",
  join(file.etags, " ") AS "Tags",
  dateformat(file.mtime, "MMM d, yy h:mm a") AS "Modified"
FROM [[]]
SORT file.mtime DESC
```
---
```dataview
TABLE WITHOUT ID
  string(Src) + choice(Src.file.frontmatter.rating, " — " + string(Src.file.frontmatter.rating), "") AS "Source Page",
  dateformat(Src.file.mtime, "MMM d, yy") AS "Modified",
  join(file.etags, " ") AS "Tags",
  "&bull; " + join(unique(rows.item), "<br>&bull; ") AS "Cross Linked Notes"
FROM [[]]
FLATTEN file.outlinks AS ol
WHERE ol.file != null AND ol.file.path != this.file.path
FLATTEN ol.file AS t
FLATTEN string(t.link) + choice(t.frontmatter.rating, " — " + string(t.frontmatter.rating), "") AS item
GROUP BY file.link AS Src
SORT Src ASC
```
---

