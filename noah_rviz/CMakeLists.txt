cmake_minimum_required(VERSION 2.8.3)

project(noah_rviz)

find_package(catkin REQUIRED COMPONENTS
  roslaunch
  rviz
  robot_state_publisher
)

catkin_package()

roslaunch_add_file_check(launch)

install(DIRECTORY launch rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
