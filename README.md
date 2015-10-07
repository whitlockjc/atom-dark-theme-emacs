Atom Dark Theme (for Emacs)
===========================

This is a port of the Atom Dark theme from [Atom.io](https://atom.io/).  For comparison, please view the following:

* [Atom Dark UI Theme](https://atom.io/themes/atom-dark-ui)
* [Atom Dark Syntax Theme](https://atom.io/themes/atom-dark-syntax)

[![Join the chat at https://gitter.im/whitlockjc/atom-dark-theme-emacs](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/whitlockjc/atom-dark-theme-emacs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Caveats
-------

First, this is a work in progress.  I am not an Emacs guru nor do I use all of the Emacs features/modes/etc.  This theme
attempts to give an Atom feel throughtout all of Emacs but seeing as I do not use all of Emacs, there are bound to be
bugs.  The following are supported:

* Default Emacs theme faces _(There were some faces that I left untouched from the Emacs defaults.  I am sure these
need to be ported as well but I didn't see any anomalies in my usage just yet.)_
* [diff-hl](https://github.com/dgutov/diff-hl)
* [flx](https://github.com/lewang/flx)
* [guide-key](https://github.com/kai2nenobu/guide-key)
* [js2-mode](https://github.com/mooz/js2-mode) _(Atom seems to parse at a level that Emacs/js2-mode do not and those
situations will be noticeable.  Examples: number constants, regular expression contents, etc.)_
* [markdown-mode](http://jblevins.org/projects/markdown-mode/) _(Emacs seems to apply theming to more places in Markdown
* [minimap](https://github.com/dengste/minimap)
files and so it is not a 100% match but it felt wrong to remove the extra things just for the consistency of the port.)_
* [powerline](https://github.com/milkypostman/powerline)

Installation
-----------
#### From Package (Melpa)

[![MELPA](http://melpa.org/packages/atom-dark-theme-badge.svg)](http://melpa.org/#/atom-dark-theme)

**M-x** `package-install` RET `atom-dark-theme`.

#### Manual

Download `atom-dark-theme.el` to the directory `~/.emacs.d/themes/`. Add this to your
`.emacs`:

```elisp
(add-to-list 'custom-theme-load-path "~/.emacs.d/themes/")
```

You can load the theme now with:

`M-x load-theme RET atom-dark`

To make it the default theme add to your `.emacs` file:

```elisp
(load-theme 'atom-dark t)
```

Configuration
-------------
#### Turn off mode specific faces

`atom-dark-theme` uses [Face Remapping](http://www.gnu.org/software/emacs/manual/html_node/elisp/Face-Remapping.html) to
better support theming of modes that do not provide their own theme faces.  _(Example: html-mode, yaml-mode, etc.)_
Whenever a mode like this is encountered, face remapping is used to alter the theme faces for the current buffer.  For
example, in `yaml-mode` YAML nodes used the `font-lock-variable-name-face` which as part of this theme renders as
`#c5c8c6` _(inherits from `default`)_ but to better match Atom Dark Theme in Atom.io it makes sense for
`font-lock-variable-name-face` to inherit from `font-lock-keyword-face` so that it renders `#96CBFE`.

For some, performing this customization could be confusing/annoying since in one mode a keyword might render one way and
in another mode it could render another way.  So to turn this off globally, just set the
`atom-dark-theme-force-faces-for-mode` variable to anything but `t`.  Here is an example:

```elisp
(setq atom-dark-theme-force-faces-for-mode nil)
```

Screenshots
-----------

To keep this page from loading slowly, screenshots have their own page:

https://github.com/whitlockjc/atom-dark-theme-emacs/tree/master/screenshots/README.md

