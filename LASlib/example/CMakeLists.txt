project ( LASexample )

include_directories (BEFORE ../inc ../../LASzip/src )

add_definitions ( -DUSE_AS_DLL )

find_library ( LAS_LIBRARY las HINTS ../src/VC12 )

add_executable ( lasexample lasexample.cpp )

target_link_libraries( lasexample ${LAS_LIBRARY} )
