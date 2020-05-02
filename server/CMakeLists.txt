# compile server
file(GLOB_RECURSE SERVER_SOURCE_FILES ${CMAKE_SOURCE_DIR}/server/src/server.c)
add_executable(${SERVER_NAME} ${SERVER_SOURCE_FILES})
target_link_libraries(${SERVER_NAME} ibverbs rdmacm rdmautils)