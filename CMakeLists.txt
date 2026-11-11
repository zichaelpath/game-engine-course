cmake_minimum_required(VERSION 3.28)
project(GameEngine CXX)

include(FetchContent)
FetchContent_Declare(sfml GIT_REPOSITORY https://github.com/SFML/SFML.git GIT_TAG 3.0.2)
FetchContent_MakeAvailable(sfml)

add_executable(GameEngine Main.cpp)
target_compile_features(GameEngine PRIVATE cxx_std_20)
target_link_libraries(GameEngine PRIVATE SFML::Graphics)