cmake_minimum_required(VERSION 3.10)
project(Rasterizer)

find_package(OpenCV REQUIRED)

add_compile_options(-w)

set(CMAKE_CXX_STANDARD 17)

set(EIGEN_SOURCE_DIR "C:/Program Files")

include_directories(${OpenCV_INCLUDE_DIRS}
                    ${EIGEN_SOURCE_DIR})

add_executable(Rasterizer main.cpp rasterizer.hpp rasterizer.cpp global.hpp Triangle.hpp Triangle.cpp Texture.hpp Texture.cpp Shader.hpp OBJ_Loader.h)
target_link_libraries(Rasterizer ${OpenCV_LIBRARIES})
#target_compile_options(Rasterizer PUBLIC -Wall -Wextra -pedantic)