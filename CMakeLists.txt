cmake_minimum_required(VERSION 3.30)

project(modules-based LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(${PROJECT_NAME} SHARED)

target_sources(${PROJECT_NAME}
    PUBLIC
    FILE_SET project_modules TYPE CXX_MODULES FILES
    modules/example.ccm
)

