
cmake_minimum_required(VERSION 2.8.3)
project(yhs_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)


## Generate messages in the 'msg' folder
add_message_files(
    FILES
    YHSStatus.msg
    YHSMotionCmd.msg
    YHSSpeakerCmd.msg
    YHSLightCmd.msg
)


## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)


catkin_package(
  CATKIN_DEPENDS
  message_runtime
  std_msgs
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
#  include
  ${catkin_INCLUDE_DIRS}
)

