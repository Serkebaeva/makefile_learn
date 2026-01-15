By default, **make** looks for a file named <ins>GNUmakefile</ins>, <ins>makefile</ins>, or <ins>Makefile</ins> (**_in that order_**).

So **from several versions of Makefile** to use **1** and **'ignore'** the others until you need them you can do:

 1. **Use the -f (File) Flag manually**<br>
 `make -f Makefile6`

 2. **Or you can run → <span style="font-size:1.4em"><em>executable <ins>run</ins></em></span>:**<br>
 use it like this:<br>
`./run 6` (Runs Makefile1)<br>
`./run 5 clean` (Runs the 'clean' target inside Makefile5)

## Only makefile6 works as expected  with `./run 6`;<br>
## makefile5 -> works with `./run 5 hellomake`, BUT with -> `./run 5` doesn't throws an error, but -> it only creates src/obj directory and doesn't create .o object files..;<br>
## makefiles 1-4 -> work only if all source code and headers are in root directory, without src and include folders...