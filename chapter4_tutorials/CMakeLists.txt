cmake_minimum_required(VERSION 2.8.3)
project(chapter4_tutorials)

find_package(catkin REQUIRED COMPONENTS
  pcl_conversions
  pcl_ros
  roscpp
  sensor_msgs
)

catkin_package(
  LIBRARIES chapter4_tutorials
  CATKIN_DEPENDS pcl_conversions pcl_ros roscpp sensor_msgs
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(my_pcl_tutorial src/c4_example3.cpp)
add_dependencies(my_pcl_tutorial ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
target_link_libraries(my_pcl_tutorial ${catkin_LIBRARIES})


