cmake_minimum_required(VERSION 2.8.12)
project(rdma_example)

if (CMAKE_BUILD_TYPE MATCHES "Debug" OR CMAKE_BUILD_TYPE MATCHES "DEBUG")
    set(COMPILE_FLAGS "-w -O0 -g3")
    message("Debug mode")
else()
    set(COMPILE_FLAGS "-w -O3 -g")
    message("Release mode")
endif()

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/out/bin) 
set(SERVER_NAME rdma_server)
set(CLIENT_NAME rdma_client)
set(COMMON_NAME rdmautils)

set(INC_DIRS ${CMAKE_SOURCE_DIR}/common/inc)

include_directories(${INC_DIRS})

add_subdirectory(common)

add_subdirectory(server)

add_subdirectory(client)
