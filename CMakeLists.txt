cmake_minimum_required(VERSION 3.5)
project(tango_icons_vendor)

find_package(ament_cmake REQUIRED)

option(INSTALL_TANGO_ICONS "Install Tango icons" OFF)
if(WIN32 OR APPLE)
  set(INSTALL_TANGO_ICONS ON)
endif()

if (INSTALL_TANGO_ICONS)
  install(DIRECTORY resource
    DESTINATION share/${PROJECT_NAME})
endif()

ament_package()
