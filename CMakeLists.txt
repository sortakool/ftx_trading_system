cmake_minimum_required(VERSION 3.22)
project(ftx_trading_system)

set(CMAKE_CXX_STANDARD 20)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

find_package(Boost 1.79.0)
find_package(Catch2)

add_executable(ftx_trading_system main.cpp)
target_link_libraries(ftx_trading_system ${CONAN_LIBS})
#target_link_libraries(ftx_trading_system boost::boost)
