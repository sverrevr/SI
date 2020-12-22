cmake_minimum_required(VERSION 3.14)

project("SI-Example-conan")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

find_package(SI CONFIG REQUIRED)

add_executable(${PROJECT_NAME}
               ${CMAKE_CURRENT_SOURCE_DIR}/../src/installation-tests/main.cc)
target_link_libraries(${PROJECT_NAME} SI::SI)
