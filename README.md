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
`media_buttons` | No | Block Inserter | [Media Buttons](action-media-buttons.md)
`post_submitbox_minor_actions` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_misc_actions` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_start` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`default_page_template_title` | Yes | N/A |
`admin_post_thumbnail_html` | No | None | [Post Thumbnail Filter](filter-admin-post-thumbnail-html.md)
`mce_css` | No | Editor Stylesheet | [MCE CSS Filter](filter-mce-css.md)
`post_gallery` | No | None | [Post Gallery Filter](filter-post-gallery.md)

## Core Features

This table documents common features within the Classic Editor, and whether they still exist or have direct Gutenberg equivalents.

Feature | Still Exists? | Gutenberg Equivalent? | Learn More
-|-|-|-
Custom Post Statuses | No | None | [Custom Post Statuses](feature-custom-post-statuses.md)
Media Tabs | No | None | [Media Tabs](feature-media-tabs.md)
Screen Options | No | None | [Screen Options](feature-screen-options.md)

## TinyMCE

This table documents common TinyMCE customizations and whether they have direct Gutenberg equivalents.

Customization | Gutenberg Equivalent? | Learn More
-|-|-
`dom.DOMUtils` | No | [TinyMCE dom.DOMUTils](tinymce-dom-domutils.md)
`Editor` | No | [TinyMCE Editor](tinymce-editor.md)
Toolbar Button | No | [TinyMCE Toolbar Button](tinymce-toolbar-button.md)
