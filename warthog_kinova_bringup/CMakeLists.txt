cmake_minimum_required(VERSION 2.8.3)
project(warthog_kinova_bringup)

find_package(catkin REQUIRED COMPONENTS)

catkin_package()

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(launch/warthog_dual_gen3_bringup.launch)
  roslaunch_add_file_check(launch/warthog_gen3_bringup.launch)
endif()

include_directories(
  ${catkin_INCLUDE_DIRS}
)
