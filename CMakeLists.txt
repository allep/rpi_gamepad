cmake_minimum_required (VERSION 2.8)
project (rpi_gamepad_driver)

#version number
set (rpi_gamepad_driver_VERSION_MAJOR 1)
set (rpi_gamepad_driver_VERSION_MINOR 0)

# Include source dir (for CMakeLists.txt)
# add_subdirectory (src)

# Include inclueds dir
include_directories(src)

file(GLOB SOURCES "src/*.cpp")
add_executable (rpi_gamepad_driver ${SOURCES})
#add_library(rpigamepad  SHARED ${SOURCES})
#add_library(rpigamepad  STATIC ${SOURCES})

# Specify which libraries to link during the build
# target_link_libraries (CMakeHelloWorld Hello)

# If needed, I can specify the position of the libraries
# set ( PROJECT_LINK_LIBS libtestStudent.so )
# link_directories( path for the dynamic libraries )
# set ( PROJECT_LINK_LIBS libtestStudent.a )
# link_directories( path for the static libraries )

# Usato per il make install
install (TARGETS rpi_gamepad_driver DESTINATION bin)

