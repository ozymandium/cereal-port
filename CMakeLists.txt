cmake_minimum_required(VERSION 2.8.3)
project(cereal_port)

find_package(catkin REQUIRED COMPONENTS roscpp)

catkin_package(
  INCLUDE_DIRS include
  LIBRARIES cereal_port
  CATKIN_DEPENDS roscpp
  DEPENDS system_lib  
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_library(cereal_port src/CerealPort.cpp)

