cmake_minimum_required(VERSION 3.15)
project(CPMSIMDJSONExample)

# ---- Dependencies ----

include(cmake/CPM.cmake)

CPMAddPackage(
  NAME simdjson
  VERSION 3.10.0
  GITHUB_REPOSITORY simdjson/simdjson
  OPTIONS
    "SIMDJSON_BUILD_STATIC_LIB ON"
)

# ---- Executable ----

add_executable(CPMSIMDJSONExample main.cpp)
target_compile_features(CPMSIMDJSONExample PRIVATE cxx_std_17)
target_link_libraries(CPMSIMDJSONExample simdjson::simdjson)

add_executable(CPMSIMDJSONExamplestatic main.cpp)
target_compile_features(CPMSIMDJSONExamplestatic PRIVATE cxx_std_17)
target_link_libraries(CPMSIMDJSONExamplestatic simdjson::simdjson_static)