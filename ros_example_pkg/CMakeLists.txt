cmake_minimum_required(VERSION 2.8.3)
project(ros_example_pkg)


find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  rosconsole
  roscpp
  roscpp_serialization
  roslib
  rostime
  std_msgs
  std_srvs
)

catkin_package()


include_directories(${catkin_INCLUDE_DIRS})

set(SOURCES src/main.cpp)


add_executable(${PROJECT_NAME}_node ${SOURCES})
target_link_libraries(${PROJECT_NAME}_node ${catkin_LIBRARIES})

