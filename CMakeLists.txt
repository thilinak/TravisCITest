cmake_minimum_required(VERSION 3.5)

if (MSVC)
	add_compile_options(/W4)
else()
	add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# GTest needs threading support
find_package (Threads)
target_link_libraries(gtest ${CMAKE_THREAD_LIBS_INIT})

add_executable(intro Main.cpp)
