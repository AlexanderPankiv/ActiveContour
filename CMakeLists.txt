cmake_minimum_required(VERSION 3.7)
project(ActiveContour)

find_package( OpenCV REQUIRED )

set(CMAKE_CXX_STANDARD 11)

include_directories(headers)

#set(HEADER_FILES
#        headers/common.h
#        headers/drlse_edge.h
#        headers/gvfc.h)

set(SOURCE_FILES
        src/common.cpp
        src/drlse_edge.cpp
        src/gvfc.cpp
        src/main.cpp)

add_executable(ActiveContour ${SOURCE_FILES} ${HEADER_FILES})

target_link_libraries( ActiveContour ${OpenCV_LIBS} )