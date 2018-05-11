cmake_minimum_required(VERSION 2.8.3)
project(mopi_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_message_files(
  FILES
  config.msg
  voltage_lvls.msg
  batt_status.msg
  mopi_info.msg
)

add_service_files(
  FILES
  MopiInfo.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

catkin_package(
  CATKIN_DEPENDS std_msgs message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
