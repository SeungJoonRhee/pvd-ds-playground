cmake_minimum_required(VERSION 3.22.1)
set(CMAKE_TOOLCHAIN_FILE="$ENV{VCPKG_ROOT}/vcpkg/scripts/buildsystems/vcpkg.cmake")
project(DSLIB)
set(CMAKE_CXX_STANDARD 14)
add_executable(main test.cpp)


find_package(absl CONFIG REQUIRED)
target_link_libraries(main PRIVATE absl::strings)

# find_package(Arrow CONFIG REQUIRED)
# target_link_libraries(main PRIVATE "$<IF:$<BOOL:${ARROW_BUILD_STATIC}>,Arrow::arrow_static,Arrow::arrow_shared>")

# find_package(Parquet CONFIG REQUIRED)
# target_link_libraries(main PRIVATE "$<IF:$<BOOL:${ARROW_BUILD_STATIC}>,Parquet::parquet_static,Parquet::parquet_shared>")