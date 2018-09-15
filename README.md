# Gutenberg Migration Guide

This repository documents WordPress Classic Editor customization points and their Gutenberg equivalents (if such exist). Its goal is to help WordPress developers update their plugins and themes for Gutenberg compatibility.

This `README.md` provides an overview to all impacted hooks (actions and filters) and TinyMCE features. Each item then has an extended document with an overview, examples of existing usage, and documentation for its Gutenberg equivalent (if any).

For the full history, see [WordPress/gutenberg#4151](https://github.com/WordPress/gutenberg/issues/4151). Please [open an issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest new hooks, usage examples, or other ideas for improvement.

Sections: [Actions & Filters](#actions--filters) | [Core Features](#core-features) | [TinyMCE](#tinymce)

## Actions & Filters

This table documents the most common actions and filters within the Classic Editor, and whether they still exist or have direct Gutenberg equivalents.

Action / Filter | Still Exists? | Gutenberg Equivalent? | Learn More
-|-|-|-
`edit_form_top` | No | None | [Edit Form Actions](action-edit-form.md)
`edit_form_after_title` | No | None | [Edit Form Actions](action-edit-form.md)
`edit_form_before_permalink` | No | None | [Edit Form Actions](action-edit-form.md)
`edit_form_after_editor` | No | None | [Edit Form Actions](action-edit-form.md)
`enter_title_here` | Yes | N/A |
`write_your_story` | Yes | N/A |
`post_updated_messages` | No | No | [Post Updated Messages Filter](filter-post-updated-messages.md)
`media_buttons` | No | Block Inserter | [Media Buttons](action-media-buttons.md)
`post_submitbox_minor_actions` | No | `PluginPostStatusInfo` | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_misc_actions` | No | `PluginPostStatusInfo` | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_start` | No | `PluginPostStatusInfo` | [Post Submitbox Actions](action-post-submitbox.md)
`default_page_template_title` | Yes | N/A |
`page_attributes_dropdown_pages_args` | No | None | [Dropdown Pages Args Filters](filter-dropdown-pages-args.md)
`quick_edit_dropdown_pages_args` | No | None | [Dropdown Pages Args Filters](filter-dropdown-pages-args.md)
`admin_post_thumbnail_html` | No | `editor.PostFeaturedImage` | [Post Thumbnail HTML Filter](filter-admin-post-thumbnail-html.md)
`admin_post_thumbnail_size` | No | `editor.PostFeaturedImage.imageSize` | [Post Thumbnail Size Filter](filter-admin-post-thumbnail-size.md)
`mce_css` | No | Enqueue Stylesheet | [MCE CSS Filter](filter-mce-css.md)
`image_send_to_editor` | No | None | [Image Send To Editor Filter](filter-image-send-to-editor.md)
`post_gallery` | No | None | [Post Gallery Filter](filter-post-gallery.md)

## Core Features

This table documents common features within the Classic Editor, and whether they still exist or have direct Gutenberg equivalents.

Feature | Still Exists? | Gutenberg Equivalent? | Learn More
-|-|-|-
Editor Stylesheets | No | Enqueue Stylesheet | [Editor Stylesheets](feature-editor-stylesheets.md)
Custom Post Statuses | No | None | [Custom Post Statuses](feature-custom-post-statuses.md)
Custom Fields Metabox | No | None | [Custom Fields Metabox](feature-custom-fields-metabox.md)
Media Tabs | No | None | [Media Tabs](feature-media-tabs.md)
Screen Options | No | None | [Screen Options](feature-screen-options.md)

## TinyMCE

This table documents common TinyMCE customizations and whether they have direct Gutenberg equivalents.

Customization | Still Exists? | Gutenberg Equivalent? | Learn More
-|-|-|-
`dom.DOMUtils` | No | None | [TinyMCE dom.DOMUTils](tinymce-dom-domutils.md)
`Editor` | No | None | [TinyMCE Editor](tinymce-editor.md)
`mce_buttons` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`mce_buttons_2` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`mce_buttons_3` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`mce_buttons_4` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`style_formats` | Partially | N/A | [TinyMCE Style Formats](tinymce-style-formats.md)
`tiny_mce_before_init` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`tiny_mce_plugins` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
`tiny_mce_external_plugins` | Yes | N/A | [TinyMCE Filters](tinymce-filters.md)
Toolbar Button | No | None | [TinyMCE Toolbar Button](tinymce-toolbar-button.md)

