cmake_minimum_required(VERSION 3.16)

project(MyIISUrlRewrite CXX)

#add_subdirectory(utils)

file(GLOB SRC_FILES 
    "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp"
    "${CMAKE_CURRENT_SOURCE_DIR}/*.h"
)

add_executable(${PROJECT_NAME} ${SRC_FILES})
#target_link_libraries(${PROJECT_NAME} ModernCppUtils fmt::fmt)
target_link_libraries(${PROJECT_NAME} PRIVATE ZLIB::ZLIB CURL::libcurl)
target_include_directories(${PROJECT_NAME} PRIVATE "." )