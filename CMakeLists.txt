cmake_minimum_required(VERSION 3.5)
project(tango_icons_vendor)

find_package(ament_cmake REQUIRED)

if (WIN32 OR APPLE OR INSTALL_TANGO_ICONS)
  install(DIRECTORY resource
    DESTINATION share/${PROJECT_NAME})
endif()

ament_package()
