cmake_minimum_required(VERSION 3.0.2)
project(mbf_costmap_core)

find_package(catkin REQUIRED
        COMPONENTS
            std_msgs
            geometry_msgs
            mbf_abstract_core
            mbf_utility
            tf
            costmap_2d
            nav_core
        )

catkin_package(
    INCLUDE_DIRS
        include
    CATKIN_DEPENDS
            std_msgs
            geometry_msgs
            mbf_abstract_core
            mbf_utility
            tf
            costmap_2d
            nav_core
)

## Install project namespaced headers
install(DIRECTORY include/${PROJECT_NAME}/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
  FILES_MATCHING PATTERN "*.h"
  PATTERN ".svn" EXCLUDE)
