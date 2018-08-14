#  COIN-OR CBC with Cmake support 

This repository includes a port of [coin-or/Cbc](https://github.com/coin-or/Cbc) with added CMake support in the `/Cbc` folder.

CBC is an open-source MILP solver. It uses many of the COIN-OR components and is designed to be used with CLP. It is available as a library and as a standalone solver.

## How to install
```
cd Cbc
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=RELEASE -DCMAKE_INSTALL_PREFIX=/usr/local/
make -j6
make install
```

## How to use in other projects
```
find_package(coinorcbc REQUIRED)
target_link_libraries(${YOUR_TARGET_NAME}
PRIVATE
    libCbc libCgl libOsiClp libOsi libClp libCoinUtils
)
```