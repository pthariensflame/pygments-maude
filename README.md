# Pygments lexers for Maude

This [Python](https://www.python.org) module provides
[Pygments](http://pygments.org) lexers for the
[Maude](http://maude.cs.illinois.edu/w/index.php?title=The_Maude_System)
language and its interactive environment.

In order to use these on the command line, pass the parameter `-l
/path/to/pygments_maude.py:MaudeLexer -x` (for batch Maude code) or
`-l /path/to/pygments_maude.py:MaudeLogLexer -x` (for Maude system
interaction logs) to the `pygmentize` comand in place of a language
flag (where *`/path/to/pygments_maude.py`* should be replaced by the
actual local path to the file `pygments_maude.py` from this
repository).

In order to use this with [LaTeX](http://www.latex-project.org) and
[`minted`](https://github.com/gpoore/minted),
