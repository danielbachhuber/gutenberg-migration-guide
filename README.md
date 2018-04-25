# Gutenberg Migration Guide

This repository documents integration points in the WordPress Classic Editor and their Gutenberg equivalents (if such exist). Its goal is to help WordPress developers update their projects for Gutenberg compatibility.

For the full history, see [WordPress/gutenberg#4151](https://github.com/WordPress/gutenberg/issues/4151). Please [open an issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) for questions, to suggest improvements, etc.

Sections: [Actions](#actions) | [TinyMCE](#tinymce)

## Actions

This table documents the most common actions within the Classic Editor, and whether they still exist or have direct Gutenberg equivalents.

Action | Still Exists? | Direct Equivalent? | Learn More
-|-|-|-
`edit_form_after_title` | No | None | [Reference](action-edit-form.md)
`edit_form_before_permalink` | No | None | [Reference](action-edit-form.md)
`edit_form_after_editor` | No | None | [Reference](action-edit-form.md)
`media_buttons` | No | Inserter | [Reference](action-media-buttons.md)
`post_submitbox_minor_actions` | No | None | [Reference](action-post-submitbox.md)
`post_submitbox_misc_actions` | No | None | [Reference](action-post-submitbox.md)
`post_submitbox_start` | No | None | [Reference](action-post-submitbox.md)
`admin_post_thumbnail_html` | No | None | [Reference](action-admin-post-thumbnail-html.md)

## TinyMCE

This table documents common TinyMCE customizations and whether they have direct Gutenberg equivalents.

Customization | Direct Equivalent? | Learn More
-|-|-
Toolbar Button | | [Reference](tinymce-toolbar-button.md)
