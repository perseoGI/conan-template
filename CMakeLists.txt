cmake_minimum_required(VERSION 3.15)
project(myapp CXX)

find_package(spdlog CONFIG REQUIRED)

add_executable(myapp src/main.cpp)

target_link_libraries(myapp PRIVATE spdlog::spdlog)

install(TARGETS myapp DESTINATION "."
        RUNTIME DESTINATION bin
        ARCHIVE DESTINATION lib
        LIBRARY DESTINATION lib
        )
