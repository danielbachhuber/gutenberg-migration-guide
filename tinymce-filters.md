# TinyMCE Filters

Covers the following filters:

* `mce_buttons`
* `mce_buttons_2`
* `mce_buttons_3`
* `mce_buttons_4`
* `tiny_mce_before_init`
* `tiny_mce_plugins`
* `tiny_mce_external_plugins`

## Overview

A variety of filters (listed above) run in the Classic Editor prior to TinyMCE initialization. These filters permit customization of the TinyMCE instance.

## Examples

One existing use is the [Hawaiian Characters](https://wordpress.org/plugins/hawaiian-characters/) plugin which registers custom characters via the `charmap_append` setting:

![image](https://user-images.githubusercontent.com/1238696/42661478-2a8b1be0-85e3-11e8-8449-bf9cb4160dc9.png)

```php
/**
 * add new characters to end of charmap
 */
function hc_tinymce_init( $settings ) {
	$new_chars = json_encode( array(
		array( '0256', 'A - kahako' ),
		array( '0257', 'a - kahako' ),
		array( '0274', 'E - kahako' ),
		array( '0275', 'e - kahako' ),
		array( '0298', 'I - kahako' ),
		array( '0299', 'i - kahako' ),
		array( '0332', 'O - kahako' ),
		array( '0333', 'o - kahako' ),
		array( '0362', 'U - kahako' ),
		array( '0363', 'u - kahako' ),
		array( '0699', 'okina' ),
	) );
	$settings['charmap_append'] = $new_chars;

	return $settings;
}
```

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

All of the listed filters also run when TinyMCE is initialized for Gutenberg.
