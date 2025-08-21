+++
title = "TIL: Zola shortcodes can accept named parameters"
date = 2025-01-15
description = "Quick discovery about Zola's shortcode flexibility"

[taxonomies]
tags = ["zola", "web-dev", "til"]

[extra]
kind = "TIL"
+++

Was struggling with passing complex data to shortcodes, then discovered you can do:

Game changer for my image galleries! No more positional parameter confusion.

Also learned you can mix positional and named:

```
{{ image_gallery("folder/path", alt="Gallery description", lazy=true) }}
```

The Zola docs mention this but it's easy to miss. Sometimes the best discoveries come from frustration with the "obvious" way not working.
