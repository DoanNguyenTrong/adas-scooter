cmake_minimum_required(VERSION 3.10)
project(adas_scooter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# -Wall -I/usr/lib/opencv simple_camera.cpp -L/usr/lib -lopencv_core -lopencv_highgui -lopencv_videoio -o simple_camera
# add_compile_options(-Wall -I/usr/include/opencv4  -L/usr/lib -lopencv_core -lopencv_highgui -lopencv_videoio)

find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )


add_executable(adas_scooter src/adas_scooter.cpp)

target_link_libraries( adas_scooter ${OpenCV_LIBS} )

