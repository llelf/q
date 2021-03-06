# CoreHackers::Q

QAST tree visualizer

# DESCRIPTION

Installs `q-corehackers.p6` command line script that parses out QAST trees
from a program and makes an HTML file from them.

The HTML page provides these extra features unavailable in plain
`perl6 --target=ast` and `perl6 --target=optimize` output:

* Click on individual tree nodes to collapse/expand them
* Color coding: of sunk nodes, QAST::Want alternatives, static and non-static
    calls, etc.

Sample of the generated page can be seen here: https://temp.perl6.party/pub/corehackers-q-sample.html

Example output:
![](example.png)

# USAGE

```
    Usage:
      q-corehackers.p6 a '[<args> ...]'
      q-corehackers.p6 o '[<args> ...]'
```

## `a` command

```bash
$ q-corehackers.p6 a perl6 -e 'say "hello"' > out.html; google-chrome out.html
```

`a` stands for `--target=ast` and the args that follow is a `perl6` invocation
 to run the script (the `--target=ast` argument will be inserted automatically).

The script will parse QAST generated by the given `perl6` program and output
an HTML file to STDOUT. View the file in any browser to examine the QAST tree.

## `o` command

```bash
$ q-corehackers.p6 o perl6 -e 'say "hello"' > out.html; google-chrome out.html
```

`o` stands for `--target=optimize`. Same as `a`, except parses
`--target=optimize` QAST. Once again, you don't need to manually specify
`--target` parameter.

----

#### REPOSITORY

Fork this module on GitHub:
https://github.com/zoffixznet/q

#### BUGS

To report bugs or request features, please use
https://github.com/zoffixznet/q/issues

#### AUTHOR

Zoffix Znet (http://perl6.party/)

#### LICENSE

You can use and distribute this module under the terms of the
The Artistic License 2.0. See the `LICENSE` file included in this
distribution for complete details.

The `META6.json` file of this distribution may be distributed and modified
without restrictions or attribution.
