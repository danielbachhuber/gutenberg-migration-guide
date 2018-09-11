# TinyMCE Style Formats

Covers the following TinyMCE API:

* `style_formats`

## Overview

TinyMCE includes a default button which makes it possible to create UI for assigning custom inline text styles. This button (which renders as a dropdown) then appears in its registered position in the TinyMCE toolbar.

## Existing Usage

From [#12](https://github.com/danielbachhuber/gutenberg-migration-guide/issues/12), the following screenshot depicts a style select dropdown that allows for different inline text markup:

![image](https://user-images.githubusercontent.com/15941266/45097398-163f0280-b123-11e8-9ae2-1e9c66d3a417.png)

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

While Gutenberg's implementation of the Classic Block will include the style select dropdown, there isn't a way to offer an equivalent experience for other rich-text editing experiences.

See these issues for related conversation:

* [#4658 TinyMCE Custom Buttons and Extensibility](https://github.com/WordPress/gutenberg/issues/4658)
