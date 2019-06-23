I was googling for the solution of a problem: how to convert and ASCII report, with color, to html from the Linux/\*nix cli. Initially pip-installed ansi2html and tried that and it's really nice, except that I need a fixed-width/monospaced font so things would line up and ansi2html gave me a variable-width font with no options to change that.

After a quick search I discovered that Vim comes bundled with yet another plug-in, 2html, invoked via `:TOhtml`. 

These bash scripts will invoke Vim and 2html for 2 use-cases:

1. **vansi2html**
```
Usage:

$ vanis2html foo.txt
```

This would create foo.txt.html in the same directory. Use this to convert ANSI color escape codes to html.

2. **vsyntax2html**
```
Usage:

$ vsyntax2html foo.java
```

This would create foo.java.html in the same directory. Use this to get syntax syntax highlighting converted to html.
