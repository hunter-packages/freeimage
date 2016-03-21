cmake_minimum_required(VERSION 3.0)

include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/ruslo/hunter/archive/v0.14.4.tar.gz"
    SHA1 "7a8ec9a01204a294e44de37e800db41fda477af2"
)

project(FreeImage VERSION 3.17.0)

hunter_add_package(ZLIB)
find_package(ZLIB CONFIG REQUIRED)

hunter_add_package(PNG)
find_package(PNG CONFIG REQUIRED)

hunter_add_package(TIFF)
find_package(TIFF CONFIG REQUIRED)

hunter_add_package(Jpeg)
find_package(JPEG CONFIG REQUIRED)

add_library(freeimage)

target_link_libraries(freeimage PUBLIC ZLIB::zlib)
target_link_libraries(freeimage PUBLIC PNG::png)
target_link_libraries(freeimage PUBLIC TIFF::libtiff)
target_link_libraries(freeimage PUBLIC JPEG::jpeg)
