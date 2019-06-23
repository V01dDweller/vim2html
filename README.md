**The problem:** How to quickly convert an ASCII file with color escapes to html via the cli or bash scripts.

Initially, [ansi2html](https://pypi.org/project/ansi2html/) was the solution and while it is really well done, a fixed-width/mono-spaced font was needed so things like logs, tables or reports would line up. Unfortunately, html renders by default with a variable-width font and ansi2html has no obvious way to change it.

It just so happens that Vim comes bundled with a  plug-in, [2html](https://github.com/vim/vim/blob/master/runtime/syntax/2html.vim).vim, (See the [:TOhtml](http://vimdoc.sourceforge.net/htmldoc/syntax.html#:TOhtml) command) which, in combination with [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302) and a bash script, solves the problem nicely.

**Note:** This won't work without first installing [:AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302).

**Installation**

Copy these to a directory in your PATH. e.g. ~/bin, $HOME/bin, etc.

**Examples:**

1. **vansi2html** - Converting ANSI with color escapes:
```
Usage:

$ vanis2html foo.txt

Created foo.txt.html

```

**Bonus:**
2. **vsyntax2html** - Convert syntax highlighting to html:
```
Usage:

$ vsyntax2html foo.java

Created foo.java.html

```
