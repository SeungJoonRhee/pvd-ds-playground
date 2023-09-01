# Requirements
Need to have Cmake and VCPKG installed. Requires VCPKG_ROOT to be set to the path to vcpkg.

# Setup Commands
```
    mkdir build
    vcpkg install
    cmake -B ./build -S . -DCMAKE_TOOLCHAIN_FILE=$VCPKG_ROOT/scripts/buildsystems/vcpkg.cmake
    cmake --build ./build
```
