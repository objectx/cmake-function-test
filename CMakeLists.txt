
cmake_minimum_required (VERSION 3.20)

project (cmake-function-test)

add_subdirectory (dir1)
add_subdirectory (dir2)

call1 ("Call 1")
call2 ("Call 2")
