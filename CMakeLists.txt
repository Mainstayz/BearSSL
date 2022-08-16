cmake_minimum_required(VERSION 3.10)
project (bearssl)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_library(bearssl  ${BUILD_LIB_TYPE} "")

target_include_directories(bearssl PUBLIC inc)

add_library(BearSSL::BearSSL ALIAS bearssl)

add_subdirectory(src)

install(TARGETS bearssl ${INSTALL_DESTINATION_TYPE})

#add_subdirectory(samples)
#add_subdirectory(tools)
#add_subdirectory(test)