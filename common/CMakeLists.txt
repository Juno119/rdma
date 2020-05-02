# compile rdmautils
file(GLOB_RECURSE COMMON_SOURCE_FILES ${CMAKE_SOURCE_DIR}/common/src/common.c)
add_library(${COMMON_NAME} SHARED ${COMMON_SOURCE_FILES})
target_link_libraries(${COMMON_NAME} ibverbs rdmacm)