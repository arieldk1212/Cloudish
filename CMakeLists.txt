cmake_minimum_required(VERSION 3.50)
project(cloudish VERSION 1.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_INCLUDE_CURRENT_DIR)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_TOOLCHAIN_FILE "${VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake")
set(CMAKE_PREFIX_PATH "vcpkg_installed/arm64-osx/share")

include_directories(inc)

find_package(imgui CONFIG REQUIRED)
find_package(GTest CONFIG REQUIRED)

list(APPEND PROJ_LIBS
imgui::imgui
GTest::gtest GTest::gtest_main
GTest::gmock GTest::gmock_main
)

add_subdirectory(src)
enable_testing()
add_subdirectory(tests)