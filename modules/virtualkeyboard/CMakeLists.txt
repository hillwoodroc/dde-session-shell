include_directories(
    global
)

link_libraries(
    ${Qt_LIBS}
)

set(LIB_NAME virtualkeyboard)

set(MODULESDIR ${CMAKE_INSTALL_LIBDIR}/dde-session-shell/modules)

aux_source_directory(. SRCS)

add_library(${LIB_NAME} SHARED ${SRCS})

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/modules)

install(TARGETS ${LIB_NAME} LIBRARY DESTINATION ${MODULESDIR})
