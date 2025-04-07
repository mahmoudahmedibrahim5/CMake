cmake_minimum_required(VERSION 3.31.1)
project(hello)

add_subdirectory(lib)

set(INCLUDE_FILES
    inc/
    lib/
)

set( SRC_FILES
    main.cpp
    src/app.cpp
)

add_executable(main ${SRC_FILES})
target_include_directories(main PUBLIC ${INCLUDE_FILES})
target_link_libraries(main PUBLIC lib)
