# vim2html #

**The problem:** Quickly converting an ASCII file with color escapes to html via the cli or bash scripts.

Initially, [ansi2html](https://pypi.org/project/ansi2html/) was the solution and while it is really well done, a fixed-width/mono-spaced font was needed so things like logs, tables or reports would line up. Unfortunately, most browsers render html with a variable-width font by default and ansi2html has no obvious way to change that.

Fortunately, Vim comes bundled with a  plug-in, [2html.vim](https://github.com/vim/vim/blob/master/runtime/syntax/2html.vim), (See the [TOhtml](http://vimdoc.sourceforge.net/htmldoc/syntax.html#:TOhtml) command) which generates html with a fixed width by using `<PRE>`. When combined with [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302) - another plug-in that is not bundled with Vim - and a tiny bash script, it solves the problem nicely.

**This will overwrite files without warning, use at your own risk!**

**Installation**

1. Install [AnsiEsc](https://www.vim.org/scripts/script.php?script_id=302)
2. Copy these to a directory in your PATH. e.g. ~/bin, $HOME/bin, etc..

**Usage:**

1. **vansi2html** - Converting ANSI with color escapes:
    ```
    $ vanis2html foo.txt
    
    Created foo.txt.html
    ```


2. **vsyntax2html** - Save Vim's syntax highlighted output to html:
    ```
    $ vsyntax2html foo.java
    
    Created foo.java.html
    ```
