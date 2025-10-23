cmake_minimum_required(VERSION 3.10)
PROJECT (cdrkit C)
if(CMAKE_SYSTEM_NAME STREQUAL "Linux" AND CMAKE_ANDROID_ARCH)
    link_libraries(android-glob android-utimes)
endif()
add_definitions("-D__THROW=")
add_definitions("-UTHREADED_CHECKSUMS")
SUBDIRS(include genisoimage wodim libedc libhfs_iso libparanoia icedax libusal librols libunls readom netscsid 3rd-party/dirsplit)

