cmake_minimum_required(VERSION 2.8.3)
project(mav_disturbance_observer)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

add_definitions(-std=c++11)
set(CMAKE_BUILD_TYPE Release)

#############
# LIBRARIES #
#############
cs_add_library(KFDisturbanceObserverLibrary
  src/KF_disturbance_observer.cpp
)

############
# BINARIES #
############

#No binaries, only libraries in this package!

##########
# EXPORT #
##########
cs_install()
cs_export()
