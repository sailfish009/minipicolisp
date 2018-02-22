minipicolisp windows port

- visual c++ 2017 express build : open picolisp.sln with vs2017 express http://aka.ms/vs/15/release/vs_WDExpress.exe


- mingw32 g++    build : using cmake (with g++, has segmentation fault bug, with vc++, it works fine)

  $ cd build/

  $ cmake ../picolisp/ -G "MinGW Makefiles"

  $ mingw32-make