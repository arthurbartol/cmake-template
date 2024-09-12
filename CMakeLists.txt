cmake_minimum_required(VERSION 3.20)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set_property(GLOBAL PROPERTY PREDEFINED_TARGETS_FOLDER "cmake")

project(ProjectName)

set(CMAKE_CXX_STANDARD 20)

add_library(${PROJECT_NAME} STATIC
    # Source files
    src/information.cpp

    # Header files
    src/include/information.h
)

target_compile_definitions(${PROJECT_NAME} PRIVATE PROJECT_NAMESPACE=${PROJECT_NAME})

add_executable(${PROJECT_NAME}
    # Source files
    src/main.cpp

    # Header files
)

target_link_libraries(${PROJECT_NAME}
    #
)
