# Gutenberg Migration Guide

This repository documents integration points in the WordPress Classic Editor and their Gutenberg equivalents (if such exist). Its goal is to help WordPress developers update their projects for Gutenberg compatibility.

This `README.md` provides an overview to all impacted hooks (actions and filters) and TinyMCE features. Each item then has an extended document with an overview, examples of existing usage, and documentation for its Gutenberg equivalent (if any).

For the full history, see [WordPress/gutenberg#4151](https://github.com/WordPress/gutenberg/issues/4151). Please [open an issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) for questions, to suggest improvements, etc.

Sections: [Hooks](#hooks) | [TinyMCE](#tinymce)

## Hooks

This table documents the most common actions and filters within the Classic Editor, and whether they still exist or have direct Gutenberg equivalents.

Action | Still Exists? | Direct Equivalent? | Learn More
-|-|-|-
`edit_form_after_title` | No | None | [Edit Form Actions](action-edit-form.md)
`edit_form_before_permalink` | No | None | [Edit Form Actions](action-edit-form.md)
`edit_form_after_editor` | No | None | [Edit Form Actions](action-edit-form.md)
`media_buttons` | No | Inserter | [Media Buttons](action-media-buttons.md)
`post_submitbox_minor_actions` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_misc_actions` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`post_submitbox_start` | No | None | [Post Submitbox Actions](action-post-submitbox.md)
`admin_post_thumbnail_html` | No | None | [Post Thumbnail Filter](action-admin-post-thumbnail-html.md)

## TinyMCE

This table documents common TinyMCE customizations and whether they have direct Gutenberg equivalents.

Customization | Direct Equivalent? | Learn More
-|-|-
Toolbar Button | | [Reference](tinymce-toolbar-button.md)
