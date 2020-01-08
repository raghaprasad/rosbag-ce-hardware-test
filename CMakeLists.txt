cmake_minimum_required(VERSION 2.8.3)
project(rosbag_ce_hardware_tests_ros1)

find_package(catkin REQUIRED COMPONENTS rospy)

catkin_package(
        LIBRARIES rosbag_ce_hardware_tests_ros1
)
#############
## Install ##
#############
install(PROGRAMS
        tests/test_rosbag_uploader_ros1.py
        DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY configurations launch
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
