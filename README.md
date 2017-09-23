# Pygments Lexers for Maude

This [Python](https://www.python.org) module provides
[Pygments](http://pygments.org) lexers for the
[Maude](http://maude.cs.illinois.edu/w/index.php?title=The_Maude_System)
language and its interactive environment.

## Command-Line Usage

In order to use these on the command line, pass the parameter `-l
/path/to/pygments_maude.py:MaudeLexer -x` (for batch Maude code) or
`-l /path/to/pygments_maude.py:MaudeLogLexer -x` (for Maude system
interaction logs) to the `pygmentize` comand in place of a language
flag (where `/path/to/pygments_maude.py` should be replaced by the
actual local path to the file
[`pygments_maude.py`](https://raw.githubusercontent.com/pthariensflame/pygments-maude/master/pygments_maude.py)
from this repository).

## LaTeX/`minted` Usage

In order to use this with [LaTeX](http://www.latex-project.org) and
[`minted`](https://github.com/gpoore/minted), put the following lines
into your document preamble:

``` latex
\usepackage{xparse}
\NewExpandableDocumentCommand\maudeLexer{}{pygments_maude.py:MaudeLexer -x}
\NewExpandableDocumentCommand\maudeLogLexer{}{pygments_maude.py:MaudeLogLexer -x}
```

Then place the the file
[`pygments_maude.py`](https://raw.githubusercontent.com/pthariensflame/pygments-maude/master/pygments_maude.py)
from this repository into the same directory as your document; you
should now be able to use `\maudeLexer` and `\maudeLogLexer` as
languages recognized by all `minted` commands. (Note that this will
require a fairly recent version of `minted`, as well as a TeX install
that supports [LaTeX3](https://www.latex-project.org/latex3/).)
