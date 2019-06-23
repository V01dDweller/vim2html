**The problem:** How to quickly convert an ASCII file with color escapes to html from the Linux/\*nix cli or in bash scripts.

Initially, ansi2html was the solution and while it is really nice, a fixed-width/mono-spaced font was needed so things like logs would line up. Unfortunately, the html defaulted to a variable-width font and no obvious way to change.

After some searching I discovered that Vim comes bundled with yet another plug-in, [2html](https://github.com/vim/vim/blob/master/runtime/syntax/2html.vim).vim, invoked via [:TOhtml](http://vimdoc.sourceforge.net/htmldoc/syntax.html#:TOhtml): and in combination with the [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302) plugin would do the trick.

**Note:** This won't work without first installing [:AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302).

These bash scripts will invoke Vim and 2html.vim for 2 use-cases:

1. **vansi2html**
```
Usage:

$ vanis2html foo.txt
```

This would create foo.txt.html in the same directory. Use this to convert ANSI color escape codes to html.

**Bonus:**
2. **vsyntax2html**
```
Usage:

$ vsyntax2html foo.java
```

This would create foo.java.html in the same directory. Use this to get syntax syntax highlighting converted to html.
