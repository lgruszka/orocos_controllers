cmake_minimum_required(VERSION 2.8.6)
project(limit_detector)

find_package(catkin REQUIRED COMPONENTS rtt_ros cmake_modules)

find_package(OROCOS-RTT REQUIRED)
include(${OROCOS-RTT_USE_FILE_PATH}/UseOROCOS-RTT.cmake)

find_package(Eigen REQUIRED)

include_directories(
  ${catkin_INCLUDE_DIRS}
  ${USE_OROCOS_INCLUDE_DIRS}
  ${Eigen_INCLUDE_DIRS})
link_directories(
  ${catkin_LIBRARY_DIRS}
  ${USE_OROCOS_LIBRARY_DIRS})

find_package(OROCOS-RTT REQUIRED rtt-scripting)
orocos_component(${PROJECT_NAME} src/LimitDetector.cpp )
target_link_libraries(${PROJECT_NAME} ${catkin_LIBRARIES})
target_link_libraries(${PROJECT_NAME} ${OROCOS-RTT_RTT-SCRIPTING_LIBRARY} )

orocos_generate_package()
