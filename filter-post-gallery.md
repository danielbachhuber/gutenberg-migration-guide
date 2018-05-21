# Post Gallery Filter

Covers the following filters:

* `post_gallery`

## Overview

This filter fires when a `[gallery]` shortcode is rendered.

The Gutenberg Gallery Block does not fire this filter when displaying a gallery.

## Existing Usage

From [WordPress/gutenberg#5972](https://github.com/WordPress/gutenberg/issues/5972): The WP Gallery Custom Links plugin adds a "Gallery Link URL" field when editing gallery images so users are able to create galleries which link to external resources.

![image](https://user-images.githubusercontent.com/36432/40310397-7348c83c-5cc1-11e8-8560-109e9b21e3ba.png)

The WP Gallery Custom Links plugin continues to work on the backend with Gutenberg active, but links are ignored on the frontend.

---

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

There are no Gutenberg equivalents for this filter.
