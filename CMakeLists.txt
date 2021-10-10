cmake_minimum_required(VERSION 3.10)
project(plan)
 
find_package(ompl REQUIRED)
find_package(Boost REQUIRED COMPONENTS program_options)

set(CMAKE_CXX_STANDARD 20)

include_directories(${Boost_INCLUDE_DIR} ${OMPL_INCLUDE_DIRS})

add_executable(plan GeometricCarPlanning.cpp)
target_link_libraries(plan ${Boost_LIBRARIES} ${OMPL_LIBRARIES})
