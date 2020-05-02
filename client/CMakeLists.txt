
# compile client
file(GLOB_RECURSE CLIENT_SOURCE_FILES ${CMAKE_SOURCE_DIR}/client/src/client.c)
add_executable(${CLIENT_NAME} ${CLIENT_SOURCE_FILES})
target_link_libraries(${CLIENT_NAME} ibverbs rdmacm rdmautils)