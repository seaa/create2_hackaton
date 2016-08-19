cmake_minimum_required(VERSION 2.8.3)
project(wall_detector)

find_package(catkin REQUIRED COMPONENTS
  irobotcreate2
  rospy
  std_msgs
  message_generation
)

add_message_files(
  DIRECTORY msg
  FILES Walls.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS irobotcreate2 rospy std_msgs message_runtime
)

## Specify additional locations of header files
## Your package locations should be listed before other locations
# include_directories(include)
include_directories(
  ${catkin_INCLUDE_DIRS}
)
