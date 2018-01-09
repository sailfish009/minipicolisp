minipicolisp windows port

- visual c++ 2015 build : open picolisp.sln with vs2015


- mingw32 g++    build : using cmake (with g++, has segmentation fault bug, with vc++, it works fine)

  $ cd build/

  $ cmake ../picolisp/ -G "MinGW Makefiles"

  $ mingw32-make