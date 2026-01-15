By default, **make** looks for a file named GNUmakefile, makefile, or Makefile (in that order).

So from several versions of Makefile to use one and 'ignore' the others until you need them you can do:

 1. **Use the -f (File) Flag manually**
`make -f Makefile1`

 2. **Or you can run executable 'run'** <br> -> use it like this: <br>
`./run 1` (Runs Makefile1) <br>
`./run 2 clean` (Runs the 'clean' target inside Makefile2)