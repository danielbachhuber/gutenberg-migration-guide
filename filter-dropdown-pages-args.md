# Dropdown Pages Args Filters

Covers the following filters:

* `page_attributes_dropdown_pages_args`
* `quick_edit_dropdown_pages_args`

## Overview

The `page_attributes_dropdown_pages_args` and `quick_edit_dropdown_pages_args` filters fire when generating the list of pages available when selecting a post's parent. It's a documented way of modifying the pages available.

## Existing Usage

One existing used defined in [WordPress/gutenberg#9089](https://github.com/WordPress/gutenberg/issues/9089) is:

> By using the filters, it is possible with Quick-Edit or Classic Editor to edit parent relations also for draft pages. This is important for some workflows because it may be necessary to create the whole structure before publishing. Unfortunately using the Gutenberg Preview functions deletes parent-relations for Draft-Pages.

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

There are no Gutenberg equivalents for this filter. See [WordPress/gutenberg#9089](https://github.com/WordPress/gutenberg/issues/9089) for discussion on how to accommodate.
