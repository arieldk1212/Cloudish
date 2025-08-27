enable_testing()
include(GoogleTest)

# Cloudish
add_executable(
  CloudishTest
  CloudishTest.cpp
)
target_link_libraries(
  CloudishTest
  ${PROJ_LIBS}
)
gtest_discover_tests(CloudishTest)