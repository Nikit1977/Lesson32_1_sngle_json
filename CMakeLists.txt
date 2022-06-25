cmake_minimum_required(VERSION 3.22)
project(3_protoc)

set(CMAKE_CXX_STANDARD 17)
set(JSON_BuildTests OFF CACHE INTERNAL "")

add_subdirectory(nlohmann_json)
include_directories(protobuf-3.21.1/src/google/protobuf)

add_executable(3_protoc main.cpp)

target_link_libraries(3_protoc PRIVATE nlohmann_json::nlohmann_json)
