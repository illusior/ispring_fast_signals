cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

project(FastSignals)

# Use `-DBUILD_TESTING=OFF` to disable testing/benchmarking.
enable_testing()

include(cmake/functions.cmake)

add_subdirectory(libfastsignals)

if(BUILD_TESTING)
    add_subdirectory(tests/libfastsignals_stress_tests)
    add_subdirectory(tests/libfastsignals_unit_tests)
endif()
