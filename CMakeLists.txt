cmake_minimum_required(VERSION 2.8.3)
project(core_msgs)

find_package(catkin REQUIRED COMPONENTS geometry_msgs message_generation std_msgs)

add_message_files(
  DIRECTORY msg
  FILES
  ImuRaw.msg
  Proximity.msg
  Vector3_32.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)
