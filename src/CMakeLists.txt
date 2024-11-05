file(GLOB_RECURSE SRC_FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

set(SOURCE ${SRC_FILES})

find_package(fmt  REQUIRED)
add_executable(Clothesline ${SOURCE})

target_include_directories(Clothesline PUBLIC include)
target_link_libraries(Clothesline PUBLIC   fmt::fmt pthread)

set_target_properties(Clothesline PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)
