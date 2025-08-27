list(APPEND SRC
Cloudish.cpp
)

add_library(src STATIC ${SRC})

add_executable(Cloudish ${SRC})

target_link_libraries(Cloudish PRIVATE src ${PROJ_LIBS})