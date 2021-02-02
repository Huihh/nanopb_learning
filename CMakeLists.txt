
cmake_minimum_required(VERSION 3.13)


project(hello)


add_subdirectory(lib)

add_executable(hello main.c simple.pb.c)


target_link_libraries(hello PUBLIC my_nanopb)

target_include_directories(hello PUBLIC 
    "${PROJECT_SOURCE_DIR}"
    "${PROJECT_SOURCE_DIR}/lib"
)







