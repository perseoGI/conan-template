cmake_minimum_required(VERSION 3.15)
project(myapp CXX)

# Find required packages
find_package(spdlog CONFIG REQUIRED)
find_package(ZLIB REQUIRED)

# Create compression library
add_library(compression
    src/compression.cpp
    src/compression.h
)

target_link_libraries(compression PUBLIC
    ZLIB::ZLIB
    spdlog::spdlog
)

target_include_directories(compression PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/src
)

# Main executable
add_executable(myapp src/main.cpp)

target_link_libraries(myapp PRIVATE
    compression
    spdlog::spdlog
    ZLIB::ZLIB
)


include(CTest)
if (BUILD_TESTING)
    add_subdirectory(tests)
endif()
