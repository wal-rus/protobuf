This directory contains example code that uses Protocol Buffers to manage an
address book.  Two programs are provided, each with three different
implementations, one written in each of C++, Java, and Python.  The add_person
example adds a new person to an address book, prompting the user to input
the person's information.  The _list_people_ example lists people already in the
address book.  The examples use the exact same format in all three languages,
so you can, for example, use _add_person_java_ to create an address book and then
use _list_people_python_ to read it.

You must install the protobuf package before you can build these.

To build all the examples (on a unix-like system), simply run "make".  This
creates the following executable files in the current directory:
  * add_person_cpp
  * list_people_cpp
  * add_person_java
  * list_people_java
  * add_person_python
  * list_people_python

If you only want to compile examples in one language, use `make cpp`,
`make java`, or `make python`.

All of these programs simply take an address book file as their parameter.
The add_person programs will create the file if it doesn't already exist.

These examples are part of the Protocol Buffers tutorial, located at:
  https://developers.google.com/protocol-buffers/docs/tutorials

Note that on some platforms you may have to edit the Makefile and remove
"-lpthread" from the linker commands (perhaps replacing it with something else).
We didn't do this automatically because we wanted to keep the example simple.

## CMake ##
CMake builds for C++ are also supported, though have only been tested on Windows.
For more information on supported CMake specific build flags and a detailed
example of how to generate code and link with protobuf using CMake, see
CMakeLists.txt.
## Go ##

The Go example requires a plugin to the protocol buffer compiler, so it is not
built with all the other examples.  See:
  https://github.com/golang/protobuf
for more information about Go protocol buffer support.

First, install the Protocol Buffers compiler (protoc).
Then, install the Go Protocol Buffers plugin
($GOPATH/bin must be in your $PATH for protoc to find it):
```
go get github.com/golang/protobuf/protoc-gen-go
```
See the instructions for building examples in one language above for more information.
