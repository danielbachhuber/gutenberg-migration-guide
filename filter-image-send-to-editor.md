# Image Send To Editor Filter

Covers the following filters:

* `image_send_to_editor`

## Overview

This filter fires when an image is being inserted into the Classic Editor. It's a [documented way](https://developer.wordpress.org/reference/hooks/image_send_to_editor/) to modify the image HTML markup used for the image.

## Existing Usage

One existing used defined in [WordPress/gutenberg#8472](https://github.com/WordPress/gutenberg/issues/8472) is:

> When the image is inserted into the post, the Pinterest Text for the image is included as a `data-pinterest-description` data attribute.

```php
/**
 * Append Pinterest Text to markup sent to editor
 *
 * @param string $html The image HTML markup to send.
 * @param int    $id   The attachment id.
 * @return string
 */
public static function filter_image_send_to_editor( $html, $id ) {
	if ( ! empty( $_POST['props']['tp_pinterest_text'] ) ) {
		$html = str_replace( '<img ', '<img data-pin-description="' . esc_attr( wp_unslash( $_POST['props']['tp_pinterest_text'] ) ) . '" ', $html );
	}
	if ( ! empty( $_POST['props']['tp_pinterest_nopin'] ) ) {
		$html = str_replace( '<img ', '<img data-pin-nopin="true" ', $html );
	}
	return $html;
}
```

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

There are no Gutenberg equivalents for this filter. See conversation in [WordPress/gutenberg#8472](https://github.com/WordPress/gutenberg/issues/8472) for discussion on how to replicate.
