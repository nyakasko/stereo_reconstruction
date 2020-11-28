# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("stereo_reconstruction")
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( stereo_reconstruction stereo_reconstruction.cpp )
target_link_libraries( stereo_reconstruction ${OpenCV_LIBS} )
