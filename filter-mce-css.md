# MCE CSS Filter

Covers the following filters:

* `mce_css`

## Overview

The `mce_css` filter fires as TinyMCE is loading. It's a [documented way](https://codex.wordpress.org/Plugin_API/Filter_Reference/mce_css) to filter the list of stylesheets to load in TinyMCE.

Gutenberg does not have a direct equivalent, although editor stylesheets can be adapted to achieve the same result.

## Existing Usage

From the [WordPress Codex](https://codex.wordpress.org/Plugin_API/Filter_Reference/mce_css), here's an example of loading the Lato font:

```php
function wpdocs_mce_css( $mce_css ) {
	if ( ! empty( $mce_css ) )
		$mce_css .= ',';

	$font_url = 'https://fonts.googleapis.com/css?family=Lato:300,400,700';
	$mce_css .= str_replace( ',', '%2C', $font_url );

	return $mce_css;
}
add_filter( 'mce_css', 'wpdocs_mce_css' );
```

---

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

While Gutenberg doesn't have a direct equivalent, remote stylesheets can be loaded using `@import()` statements.

Given an `editor-style.css` file in your theme root:

```css
@import url('https://fonts.googleapis.com/css?family=Lato:300,400,700');

// Make sure to scope your styles to Gutenberg.
.gutenberg h2 {
	font-family: Lato;
}
```

Then, in your `functions.php` file, register the `editor-style.css` file:

```php
function wpdocs_theme_add_editor_styles() {
	wp_enqueue_style( 'my-editor-stylesheet', get_stylesheet_directory_uri() . '/editor-style.css' );
}
add_action( 'enqueue_block_assets', 'wpdocs_theme_add_editor_styles' );
```

For more information, check out "[Applying Styles With Stylesheets](https://wordpress.org/gutenberg/handbook/blocks/applying-styles-with-stylesheets/)" in the Gutenberg handbook.
