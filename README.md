# viv-prj-gen

Vivado projects can be hard to version control.  The goal of this project is to make that easier by automating generation of vivado projects, to have a similar process for nonproject builds using vivado, and to automate generation of the ipxact meta data (components.xml and xgui).  This is meant to be crossplatform, but only has been tested on linux.

tcl scripts invoked through calls to functions in an included cmake file.

To use it, create your own CMakeLists.txt, include viv-prj-gen/functions.cmake, and use the provided cmake functions.  There are examples in the demos directory.

Vivado's cmake version is too old to work with functions.cmake.  Make a build directory. Use your system's /usr/bin/cmake instead of vivado's.  After invoking cmake, use make help to see targets.