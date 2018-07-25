# Post Thumbnail Size Filter

Covers the following filters:

* `admin_post_thumbnail_size`

## Overview

This filter fires when generating the image to be displayed in the Featured Image meta box. It's [documented in the WordPress developer handbook](https://developer.wordpress.org/reference/hooks/admin_post_thumbnail_size/).

## Existing Usage

One existing used defined in [WordPress/gutenberg#7505](https://github.com/WordPress/gutenberg/issues/7505) is:

> For a UX best practice I want to show the same size version of the image in the admin as on the frontend. And for listing pages, I sometimes use specific other or custom image sizes. That's what I want to be able to reflect in the admin as well.

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

[PostFeaturedImage](https://github.com/WordPress/gutenberg/tree/master/editor/components/post-featured-image) is a React component used to render the Post Featured Image selection tool.
It includes a wp.hooks filter `editor.PostFeaturedImage.imageSize` (introduced in Gutenberg v3.4 with [WordPress/gutenberg#8196](https://github.com/WordPress/gutenberg/pull/8196)) that enables developers to define a custom size for the image displayed.

_Example:_

```
var withImageSize = function( size, mediaId, postId ) {
	return 'large';
};

wp.hooks.addFilter( 'editor.PostFeaturedImage.imageSize', 'my-plugin/with-image-size', withImageSize );
```
