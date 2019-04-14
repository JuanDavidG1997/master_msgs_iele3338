cmake_minimum_required(VERSION 2.8.3)
project(master_msgs_iele3338)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
  Obstacle.msg
  Covariance.msg
)

add_service_files(
  FILES
  AckService.srv
  EndService.srv
  StartService.srv
)

generate_messages(
  DEPENDENCIES 
  geometry_msgs
)

catkin_package(
   CATKIN_DEPENDS geometry_msgs message_runtime
)
