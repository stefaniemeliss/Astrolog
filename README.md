# Astrolog 7.70

This is a copy of the "official" version of Astrolog 7.70 (released April 23, 2024) described at: http://www.astrolog.org/astrolog.htm

The files here were copied from: http://www.astrolog.org/ftp/ast77src.zip

The changes in version 7.70 are described at: http://www.astrolog.org/ftp/updat770.htm

No modifications have been made to any of these files, and the only addition is this GITHUB format README.

Compiling Astrolog
------------------

This is the easiest step. The following commands will compile the source code into object files and link those object files together with the required library or libraries to produce your very own binary executable file.

For compilation without X11 support, use the following command string and
wait a few seconds for it to complete:

gcc -c -O -Wno-write-strings -Wno-parentheses -Wno-unsequenced -Wno-constant-conversion -Wno-format *.cpp; gcc -o astrolog *.o -lm

For compilation with X11 support, use the following command string and wait
a few seconds for it to complete:

gcc -I /usr/X11/include -c -O -Wno-write-strings -Wno-parentheses -Wno-unsequenced -Wno-constant-conversion -Wno-format *.cpp; gcc -o astrolog *.o -lm -lX11 -L/usr/X11/lib

If everything went well, you'll have a new executable file in the
current directory called "astrolog". A celebration is in order!

