# liblogg
Easy and fast logging library

## Getting Started
These instructions will get you a copy of the project and use it.

##  Build and Install
To build your need cmake and a c++ compiler installed in your system.
```
$ git clone https://github.com/ern123/logg.git
$ cd logg
$ mkdir build && cd build
$ cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr ..
$ cmake --build .
$ sudo cmake --install .
```

## Example
Send a simple log message to standard output.
```
logg::logger l;
l.error("My Error Message");
l.log("A Log");
l.log(logg::LEVEL_DEBUG, "My Debug Message");
```

### Building the example
Use your compiler to build and link with logg. Pass -l in g++ or clang flag to link the library.
```
$ g++ logg_example.cpp -o logg_example -llogg
```
You can also build with pkg-config.
```
$ g++ logg_example.cpp `pkg-config --libs liblogg` -o logg_example
$ ./logg_example
```
If you install logg in /usr/local you should edit PKG_CONFIG_PATH variable to recognizes
liblogg.pc archive.
```
$ export PKG_CONFIG_PATH=/usr/local
$ g++ logg_example.cpp `pkg-config --libs liblogg` -o logg_example
$ ./logg_example
```

## Contributing
Contributors are always welcome!, all pull requests will be revised.

## License
This project is licensed under the LGPL License - see the [LICENSE](LICENSE) file for details.

## Author
Ern <ern8642@gmail.com>