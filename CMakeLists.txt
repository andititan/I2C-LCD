cmake_minimum_required(VERSION 3.5)
project(screen)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_VERBOSE_MAKEFILE ON)

# Include headers
include_directories(.)

add_executable(screen
        i2clcd.cpp
)

# Link against wiringPi
find_library(WIRINGPI_LIBRARIES NAMES wiringPi)
target_link_libraries(screen ${WIRINGPI_LIBRARIES})