get_filename_component(gl3w
    "${CMAKE_CURRENT_SOURCE_DIR}/../../../imgui/examples/libs/gl3w"
    ABSOLUTE)

add_library(gl3w STATIC
    ${gl3w}/GL/gl3w.c ${gl3w}/GL/gl3w.h ${gl3w}/GL/glcorearb.h)
target_include_directories(gl3w PUBLIC
    $<BUILD_INTERFACE:${gl3w}>)
target_link_libraries(gl3w PRIVATE ${CMAKE_DL_LIBS})
