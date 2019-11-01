cmake_minimum_required(VERSION 2.8.3)
project(warthog_ur_bringup)

find_package(catkin REQUIRED COMPONENTS)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(launch/warthog_ur_bringup.launch)
  roslaunch_add_file_check(launch/warthog_dual_ur_bringup.launch)
endif()

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
