cmake_minimum_required(VERSION 2.8.3)
project(simulation_global_fusion)

set(CMAKE_BUILD_TYPE "Release")
set(CMAKE_CXX_FLAGS "-std=c++14")
#-DEIGEN_USE_MKL_ALL")
set(CMAKE_CXX_FLAGS_RELEASE "-O3 -Wall -g")

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)

find_package(Ceres REQUIRED)

add_subdirectory(./ThirdParty/GeographicLib/)

include_directories(
  ${catkin_INCLUDE_DIRS}
  ${CERES_INCLUDE_DIRS}
  ./ThirdParty/GeographicLib/include/
)


catkin_package()


add_executable(simulation_global_fusion_node 
	src/globalOptNode.cpp
	src/globalOpt.cpp)

target_link_libraries(simulation_global_fusion_node ${catkin_LIBRARIES} ${CERES_LIBRARIES} libGeographiccc) 
