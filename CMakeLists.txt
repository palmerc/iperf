cmake_minimum_required( VERSION 3.8 )

project( iperf LANGUAGES C )

include( cmake/CMakeDebugUtils.cmake )
include( config.cmake )

set( BUILD_STATIC on )
set( BUILD_STATIC_EXE on )
set( BUILD_SHARED on )
set( BUILD_SHARED_EXE on )
set( BUILD_APPLE_FRAMEWORK off )

add_subdirectory( src )

configure_file( iperf3.spec.in iperf3.spec )
