cmake_minimum_required(VERSION 3.14)

project(Predefination LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(PREFIX_HPPHEADER *.hpp)
set(PREFIX_SOURCE *.cpp)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)


file(GLOB SOURCESFILE
    include/${PREFIX_HPPHEADER}
    src/${PREFIX_SOURCE}
)

add_executable(${PROJECT_NAME} ${SOURCESFILE})

install(TARGETS ${PROJECT_NAME} DESTINATION build/bin)
