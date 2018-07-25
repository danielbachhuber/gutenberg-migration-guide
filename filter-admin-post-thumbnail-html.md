# Post Thumbnail HTML Filter

Covers the following filters:

* `admin_post_thumbnail_html`

## Overview

This filter fires within the Featured Image meta box:

<img width="306" alt="image" src="https://user-images.githubusercontent.com/36432/39275445-22827050-489a-11e8-9153-9cf2393b9345.png">

## Existing Usage

One existing use is to filter the form output to include additional fields, which are processed on `save_post`:

<img width="307" alt="image" src="https://user-images.githubusercontent.com/36432/39275414-0018b63c-489a-11e8-9306-78d5af540798.png">

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

[PostFeaturedImage](https://github.com/WordPress/gutenberg/tree/master/editor/components/post-featured-image) is a React component used to render the Post Featured Image selection tool.
It includes a wp.hooks filter `editor.PostFeaturedImage` (introduced in Gutenberg v3.3) that enables developers to replace or extend it.

## Examples
Replace the contents of the panel:

```js
wp.hooks.addFilter( 
	'editor.PostFeaturedImage', 
	'myplugin/myhook', 
	function() { 
		return function() { 
			return wp.element.createElement( 
				'div', 
				{}, 
				'The replacement contents or components.' 
			); 
		} 
	} 
);
```

Prepend/Append to the panel contents:
```js
wp.hooks.addFilter( 
	'editor.PostFeaturedImage', 
	'myplugin/myhook', 
	function( original ) { 
		return function() { 
			return (
				wp.element.createElement( 
					'div', 
					{ key: 'outer' + Math.random() }, 
					[
						'Prepend above',
						_.extend( original( {} ), { key: 'my-key' } ),
						'Append below' 
					]
				)
			);
		} 
	} 
);
```
