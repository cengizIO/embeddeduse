# Copyright (C) 2019, Burkhard Stubert (DBA Embedded Use)
cmake_minimum_required(VERSION 3.5)

project(terminal)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5Gui)
find_package(Qt5Qml)
find_package(Qt5Quick)
find_package(Qt5SerialBus)

add_executable(
  ${PROJECT_NAME}
  main.cpp
  terminalmodel.cpp
  terminalmodel.h
  ecuproxy.cpp
  ecuproxy.h
  main.qml
  qml.qrc
)

target_link_libraries(${PROJECT_NAME} Qt5::Gui Qt5::Qml Qt5::Quick EmUse::ecucan)
