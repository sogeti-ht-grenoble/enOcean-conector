# enOcean-conector
A simple enOcean enabeled application.
The build is based on [CMake](https://cmake.org/).

##Building
###X86 Compilation
* We assume a working C++11 enabled compiler
* CMake is installed

```
git clone https://github.com/sogeti-ht-grenoble/enOcean-connector.git
mkdir build && cd build
cmake ../enOcean-connector/
make
```


### Cross compiling for [Raspberry Pi](https://www.raspberrypi.org/)
You'll need to install the cross compilation toolchain
```
git clone https://github.com/raspberrypi/tools/ --depth=1 /opt/raspberrypi
```

We assume that the toolchain is located under /opt/raspberrypi/tools folder.

```
git clone https://github.com/sogeti-ht-grenoble/enOcean-connector.git
mkdir build && cd build
cmake ../enOcean-connector/ -DPI=ON
make
```