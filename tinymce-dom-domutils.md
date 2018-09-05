# TinyMCE `dom.DOMUtils`

Covers the class of DOM manipulation APIs identified by [dom.DOMUtils](https://www.tinymce.com/docs/api/tinymce.dom/tinymce.dom.domutils/):

* `tinymce.dom.createFragment()`
* `tinymce.dom.addClass()`
* `tinymce.dom.removeClass()`
* `tinymce.dom.select()`
* etc.

## Overview

TinyMCE's `dom.DOMUtils` provides an API to the DOM within the TinyMCE editor.

It can be accessed globally (`tinymce.dom`) and also scoped to the active editor (`tinymce.activeEditor.dom`).

Some methods of object include `select()` (for selecting an element), `createFragment()` (for creating a new element), and so on.

## Existing Usage

One existing use of `dom.DOMUtils` is to programmatically manipulate post content:

```js
var innerHTML = '<!-- html-comment -->' + toolbar.element.innerHTML + '<!-- /html-comment -->';
var newEl = editor.dom.createFragment( innerHTML );
editor.dom.replace( newEl, origEl );
```

Please [open a new issue](https://github.com/danielbachhuber/gutenberg-migration-guide/issues) to suggest additional examples of existing usage.

## Gutenberg Equivalent

There isn't get an equivalent API in Gutenberg. See these issues for related conversation:

* [#3688 Expose TinyMCE editor content manipulation APIs in Gutenberg](https://github.com/WordPress/gutenberg/issues/3688)
* ~[#6648 TinyMCE editor events and transformation APIs](https://github.com/WordPress/gutenberg/issues/6648)~
