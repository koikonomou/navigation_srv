cmake_minimum_required(VERSION 2.8.3)
project(navigation_srv)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation
)

find_package(message_generation)

add_service_files(
  FILES
  navigation_srv.srv
)

generate_messages(
   DEPENDENCIES
   std_msgs
 )

catkin_package(
    CATKIN_DEPENDS message_runtime
)