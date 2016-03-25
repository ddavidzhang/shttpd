cmake_minimum_required(VERSION 3.4)
project(shttpd)

MESSAGE(STATUS "This is BINARY dir " ${HELLO_BINARY_DIR})
MESSAGE(STATUS "This is SOURCE dir "${HELLO_SOURCE_DIR})
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(SOURCE_FILES
        shttpd.h
        shttpd.c
        shttpd_error.c
        shttpd_method.c
        shttpd_mine.c
        shttpd_parameters.c
        shttpd_request.c
        shttpd_uri.c
        shttpd_worker.c)

add_executable(shttpd ${SOURCE_FILES})
TARGET_LINK_LIBRARIES(shttpd pthread)