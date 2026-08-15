---
title: Rendering fixture
description: A minimal, non-substantive post for checking technical article elements.
---

This short fixture checks a remark[^remark] and a linked source reference.[^source]

{% include figure.html
  src="/assets/images/posts/rendering-fixture/relationship.svg"
  alt="Three overlapping circles labeled Society, Software, and Data"
  width="960"
  height="480"
  caption="Figure 1. A local test image with a plain-text caption."
%}

```python
topics = ["society", "software", "data"]
```

| Element | Purpose |
| --- | --- |
| Figure | Check captions and alternative text |
| Note | Check linked endnotes and backlinks |

## Notes
{: .footnotes-heading}

[^remark]: A brief explanatory note used only to verify rendering.
[^source]: See the [Kramdown documentation](https://kramdown.gettalong.org/quickref.html#footnotes) for the supported syntax.
