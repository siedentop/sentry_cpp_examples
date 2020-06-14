project(sentry_example)
cmake_minimum_required(VERSION 3.14)

include(FetchContent)
FetchContent_Declare(crow
  GIT_REPOSITORY    https://github.com/siedentop/crow
  # Switch back to nlohmann/crow after PR #48 is merged.
  GIT_TAG           master
)
set(CROW_BUILD_TESTING OFF)
FetchContent_MakeAvailable(crow)

add_executable(example1 example1.cc)
target_link_libraries(example1 crow)
