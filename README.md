Atom Dark Theme (for Emacs)
===========================

This is a port of the Atom Dark theme from [Atom.io](https://atom.io/).  For comparision, please view the following:

* [Atom Dark UI Theme](https://atom.io/themes/atom-dark-ui)
* [Atom Dark Syntax Theme](https://atom.io/themes/atom-dark-syntax)

Caveats
-------

First, this is a work in progress.  I am not an Emacs guru nor do I use all of the Emacs features/modes/etc.  This theme
attempts to give an Atom feel throughtout all of Emacs but seeing as I do not use all of Emacs, there are bound to be
bugs.  The following are supported:

* Default Emacs theme faces _(There were some faces that I left untouched from the Emacs defaults.  I am sure these
need to be ported as well but I didn't see any anomalies in my usage just yet.)_
* [diff-hl](https://github.com/dgutov/diff-hl)
* [guide-key](https://github.com/kai2nenobu/guide-key)
* [js2-mode](https://github.com/mooz/js2-mode) _(Atom seems to parse at a level that Emacs/js2-mode do not and those
situations will be noticeable.  Examples: number constants, regular expression contents, etc.)_
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

Screenshots
-----------

To keep this page from loading slowly, screenshots have their own page:

https://github.com/whitlockjc/atom-dark-theme-emacs/tree/master/screenshots/README.md

