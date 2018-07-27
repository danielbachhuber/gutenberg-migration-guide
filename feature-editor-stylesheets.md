# Editor Stylesheets

Covers the editor stylesheet feature of the Classic Editor.

## Overview

In the Classic Editor, it's possible to register an editor-specific stylesheet using `add_editor_style()`. This is a [documented way](https://developer.wordpress.org/reference/functions/add_editor_style/) of including custom CSS to make the content editing experience much closer to the frontend experience.

## Gutenberg Equivalent

By default, Gutenberg doesn't load stylesheets registered with `add_editor_style()`.

The key difference between Gutenberg and the Classic Editor is that the Classic Editor loads within an `<iframe>` and Gutenberg does not. Because the Classic Editor loads within an `<iframe>`, stylesheets registered with `add_editor_style()` are kept isolated to the editor. However, because Gutenberg is a part of the broader page, any registered stylesheets apply to (and can unexpectedly break) the broader page.

Gutenberg's _preferred_ styling implementation is on a block-by-block basis. For more information, check out "[Applying Styles With Stylesheets](https://wordpress.org/gutenberg/handbook/blocks/applying-styles-with-stylesheets/)" in the Gutenberg handbook.

If you've decided you want to use your existing editor stylesheet, and you've verified it doesn't break in Gutenberg, you can enqueue it on the `enqueue_block_editor_assets` action:

```php
function wpdocs_theme_add_editor_styles() {
	wp_enqueue_style( 'my-editor-stylesheet', get_stylesheet_directory_uri() . '/editor-style.css' );
}
add_action( 'enqueue_block_editor_assets', 'wpdocs_theme_add_editor_styles' );
```

Related issues:

* [WordPress/gutenberg#5360 Blocks and Theme Styling Overview](https://github.com/WordPress/gutenberg/issues/5360)
