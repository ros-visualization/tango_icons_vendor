cmake_minimum_required(VERSION 3.5)
project(qt_gui_icons)

find_package(ament_cmake REQUIRED)

if (WIN32 OR APPLE OR INSTALL_QT_GUI_ICONS)
  install(DIRECTORY resource
    DESTINATION share/${PROJECT_NAME})
endif()

ament_package()
