# Post Submitbox Actions

Covers the following actions:

* `post_submitbox_minor_actions`
* `post_submitbox_misc_actions`
* `post_submitbox_start`

## Overview

These actions fire within the post submit box:

<img width="376" alt="image" src="https://user-images.githubusercontent.com/36432/39274273-495f4b02-4896-11e8-9d89-14ad4a1415f8.png">

## Existing Usage

One existing use is to include new form elements that are processed on `save_post`:

<img width="303" alt="image" src="https://user-images.githubusercontent.com/36432/39274366-95c02a98-4896-11e8-869e-47be62be2091.png">

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

The Post Status Info panel can be extended by the JS Plugins API. You can register a component which fills the `PluginPostStatusInfo` Slot with custom content. The slot is located right before the `Move to Trash` button.

<img width="313" alt="pluginpoststatusinfo" src="https://user-images.githubusercontent.com/695201/45586177-86534280-b8f2-11e8-8e57-651bf524a55e.png">

## Example
```js
const { PluginPostStatusInfo } = wp.editPost;
const { registerPlugin } = wp.plugins;

const MyPluginPostStatusInfo = () => (
	<PluginPostStatusInfo
		className="my-plugin-post-status-info"
	>
		My post status info
	</PluginPostStatusInfo>
);

registerPlugin( 'my-plugin-post-status-info', {
	render: MyPluginPostStatusInfo,
} );
```