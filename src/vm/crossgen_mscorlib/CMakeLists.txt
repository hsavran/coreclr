include(${CLR_DIR}/crossgen.cmake)

# Add back some of the macro removed by crossgen.cmake.
add_definitions(
    -DEnC_SUPPORTED
    -DFEATURE_EVENT_TRACE=1
    -DFEATURE_LOADER_OPTIMIZATION
    -DFEATURE_MULTICOREJIT
    -DFEATURE_RANDOMIZED_STRING_HASHING
    -DFEATURE_VERSIONING_LOG
)

add_definitions(-DCROSSGEN_MSCORLIB)

add_library_clr(mscorlib_crossgen ../mscorlib.cpp)
