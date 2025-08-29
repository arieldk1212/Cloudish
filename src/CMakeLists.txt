list(APPEND SRC
Cloudish.cpp
)

add_library(src STATIC ${SRC})

add_executable(Cloudish ${SRC})