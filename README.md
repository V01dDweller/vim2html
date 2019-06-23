**The problem:** How to quickly convert an ASCII file with color escapes to html from the Linux/\*nix cli or in bash scripts.

Initially, ansi2html was the solution and while it is really nice, a fixed-width/mono-spaced font was needed so things like logs, tables or reports would line up. Unfortunately, the html used a variable-width font and no obvious way to change it.

It turns out that Vim comes bundled with yet another plug-in, [2html](https://github.com/vim/vim/blob/master/runtime/syntax/2html.vim).vim, (See the [:TOhtml](http://vimdoc.sourceforge.net/htmldoc/syntax.html#:TOhtml) command) which, when combined with [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302) and a bash script, solves the problem.

**Note:** This won't work without first installing [:AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302).

**Installation**

Copy these to a directory in your PATH. e.g. ~/bin, $HOME/bin, etc.

**Examples:**

1. **vansi2html** - Converting ANSI with color escapes:
```
Usage:

$ vanis2html foo.txt
```

This would create `foo.txt.html` in the same directory.

**Bonus:**
2. **vsyntax2html** - Convert syntax highlighting to html:
```
Usage:

$ vsyntax2html foo.java
```

This would create foo.java.html in the same directory. Use this to get syntax syntax highlighting converted to html.
