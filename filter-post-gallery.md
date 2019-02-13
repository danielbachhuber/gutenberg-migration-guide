# Post Gallery Filter

Covers the following filters:

* `post_gallery`

## Overview

The `post_gallery` filter fires when a `[gallery]` shortcode is rendered. It's a [documented way](https://codex.wordpress.org/Plugin_API/Filter_Reference/post_gallery) of modifying gallery output.

The Gutenberg Gallery Block does not fire this filter when displaying a gallery.

## Existing Usage

From [WordPress/gutenberg#5972](https://github.com/WordPress/gutenberg/issues/5972): The [WP Gallery Custom Links](https://wordpress.org/plugins/wp-gallery-custom-links/) plugin adds a "Gallery Link URL" field when editing gallery images so users are able to create galleries which link to external resources.

![image](https://user-images.githubusercontent.com/36432/40310397-7348c83c-5cc1-11e8-8560-109e9b21e3ba.png)

The WP Gallery Custom Links plugin continues to work on the backend with Gutenberg active, but links are ignored on the frontend.

---

The [Slick Slider](https://wordpress.org/plugins/slick-slider/) plugin uses the `post_gallery` filter to turn native galleries into sliders:
https://github.com/tyrann0us/slick-slider/blob/761477365a31a2947f65dd19e8ffbc818c0815d9/inc/class-output.php#L39-L47

Because of the missing filter the plugin cannot simply re-use it for websites that use the Block Editor, but the code has to be rewritten to use `register_block_type()`'s `render_callback`.

---

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

There are no Gutenberg equivalents for this filter.
