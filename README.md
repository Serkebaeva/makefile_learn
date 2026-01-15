By default, **make** looks for a file named <ins>GNUmakefile</ins>, <ins>makefile</ins>, or <ins>Makefile</ins> (**_in that order_**).

So **from several versions of Makefile** to use **1** and **'ignore'** the others until you need them you can do:

 1. **Use the -f (File) Flag manually**<br>
 `make -f Makefile1`

 2. **Or you can run → <span style="font-size:1.4em"><em>executable <ins>run</ins></em></span>:**<br>
 use it like this:<br>
`./run 1` (Runs Makefile1)<br>
`./run 2 clean` (Runs the 'clean' target inside Makefile2)