# TinyMCE Toolbar Button

Covers the following TinyMCE API:

* `tinymce.activeEditor.addButton()`

## Overview

TinyMCE includes an API for registering custom buttons to its toolbar. These appear alongside existing TinyMCE rich formatting buttons. Custom buttons are used to insert and programmatically manipulate post content.

## Existing Usage

From [WordPress/gutenberg#4658](https://github.com/WordPress/gutenberg/issues/4658), the following screenshot depicts a TinyMCE button that wraps some text with an indicator to highlight it for social sharing:

![image](https://user-images.githubusercontent.com/36432/40311746-908a81e8-5cc5-11e8-86ac-cec699732f8f.png)

---

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

While the Gutenberg Block API provides UI for inserting block-level elements, there are no Gutenberg equivalents for customizing the block toolbar or programmatically manipulating post content.
