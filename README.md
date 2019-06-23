# vim2html #

**The problem:** Quickly converting an ASCII file with color escapes to html via the cli or bash scripts.

Initially, [ansi2html](https://pypi.org/project/ansi2html/) was the solution and while it is really well done, a fixed-width/mono-spaced font was needed so things like logs, tables or reports would line up. Unfortunately, html renders by default with a variable-width font and ansi2html has no obvious way to change it.

It just so happens that Vim comes bundled with a  plug-in, [2html.vim](https://github.com/vim/vim/blob/master/runtime/syntax/2html.vim), (See the [:TOhtml](http://vimdoc.sourceforge.net/htmldoc/syntax.html#:TOhtml) command) which always generates html with a fixed width by using `<PRE>`. When combined with [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302) in a tiny bash script it solves the problem nicely.

**This will overwrite files without warning, use at your own risk!**

**Prequisite:** [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302).



**Installation**

Copy these to a directory in your PATH. e.g. ~/bin, $HOME/bin, etc.

**Usage:**

1. **vansi2html** - Converting ANSI with color escapes:
```
$ vanis2html foo.txt

Created foo.txt.html
```

**Bonus:**
2. **vsyntax2html** - Save Vim's syntax highlighted output to html:
```
$ vsyntax2html foo.java

Created foo.java.html
```
