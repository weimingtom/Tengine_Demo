
cmake_minimum_required (VERSION 2.8)
project(Classify)

set( INSTALL_DIR ${TENGINE_DIR} )
set( TENGINE_LIBS tengine hclcpu)

set( Classify_SRCS classification.cpp  )

#include
include_directories(${INSTALL_DIR}/include)

#lib
link_directories(${INSTALL_DIR}/lib)

#exe
add_executable(Classify ${Classify_SRCS})
target_link_libraries(Classify ${TENGINE_LIBS} )