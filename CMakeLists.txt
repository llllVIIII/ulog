cmake_minimum_required(VERSION 3.13)

project(_ulog
    VERSION
        1.0.0
    DESCRIPTION 
        ""
)

# Make external libraries globally available
add_subdirectory(externals/CLI11)
set(JSON_BuildTests OFF)
set(JSON_Install OFF)
add_subdirectory(externals/json)

# Make ulog globally available
add_subdirectory(lib)

add_subdirectory(utils/ulog_cat)
add_subdirectory(utils/ulog_map)

# Make example application target available
add_subdirectory(example/linux)