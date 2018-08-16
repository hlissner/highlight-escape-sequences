# Highlight Escape Sequences

![screenie](highlight-escape-sequences.png)

This package highlights escaped sequences in strings, with primary support for a
wide variety of languages, and sensible defaults for languages it doesn't
support.

NOTE: This is a fork of
[highlight-escape-sequences](https://github.com/dgutov/highlight-escape-sequences)
that:

1. Add support for more languages:
   + python-mode
   + scala-mode
   + typescript-mode
   + enh-ruby-mode
   + (soon) lua-mode
   + (soon) sh-mode
2. Improve support for `emacs-lisp-mode` to include modifier+key sequences and
   (soon) magic regexp symbols.
3. Add a fallback rule for unsupported major modes.
4. Add a toggle-able buffer-local minor mode (`highlight-escape-sequences-mode`)
   to compliment a global one (`global-highlight-escape-sequences-mode`). This
   makes it easier to lazy load the plugin.
5. Fix how font-lock keywords are applied. They are now applied immediately to
   the current buffer, removing the need to restart buffers if you lazy loaded
   this package.

# Installation

This package is not on MELPA. It must be cloned manually or via quelpa or
straight.el, then enabled with:

```emacs-lisp
(use-package highlight-escape-sequences
  :hook ((prog-mode conf-mode) . highlight-escape-sequences-mode))
```

From [Doom Emacs](https://github.com/hlissner/doom-emacs).

# Why not PR it?

1. The author prefers not to break backward compatibility by changing hes-mode
   into a buffer-local mode.
2. I'm lazy! It's faster to fork'n'fix than to discuss/wait for solutions
   upstream. I'm open to PRing this, but not right now. Perhaps when this fork
   is more mature.
