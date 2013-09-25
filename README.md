whitespace-cleanup-mode.el
==========================

This Emacs library minor mode which will intelligently call `whitespace-cleanup`
before buffers are saved.

`whitespace-cleanup` is a handy function, but putting it in
`before-save-hook` for every buffer is overkill, and causes messy diffs
when editing code that did not initially have clean whitespace.

Additionally, whitespace preferences are often project-specific, and
it's inconvenient to set up `before-save-hook` in a `.dir-locals.el` file.

`whitespace-cleanup-mode` is a minor mode which calls `whitespace-cleanup`
before saving the current buffer, but only if the whitespace in the buffer
was initially clean.


Installation
=============

If you choose not to use one of the convenient
packages in [Melpa][melpa] and [Marmalade][marmalade], you'll need to
add the directory containing `whitespace-cleanup-mode.el` to your `load-path`, and
then `(require 'whitespace-cleanup-mode)`.

Usage
=====

Enable `whitespace-cleanup-mode` in an individual buffer like this:

```
M-x whitespace-cleanup-mode
```

Alternatively, enable it for a particular global mode:

```lisp
(add-hook 'ruby-mode-hook 'whitespace-cleanup-mode)
```

To enable it for an entire project, set `whitespace-cleanup-mode` to `t` in
your `.dir-locals.el` file.

[marmalade]: http://marmalade-repo.org
[melpa]: http://melpa.milkbox.net

<hr>

[![](http://api.coderwall.com/purcell/endorsecount.png)](http://coderwall.com/purcell)

[![](http://www.linkedin.com/img/webpromo/btn_liprofile_blue_80x15.png)](http://uk.linkedin.com/in/stevepurcell)

[Steve Purcell's blog](http://www.sanityinc.com/) // [@sanityinc on Twitter](https://twitter.com/sanityinc)
