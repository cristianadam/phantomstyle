cmake_minimum_required(VERSION 3.20)

project(PhantomStyle)

set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Core Widgets)
qt_standard_project_setup()

add_subdirectory(src/phantom)

option(PHANTOMSTYLE_FUNHOUSE "Build funhouse application" OFF)
if (PHANTOMSTYLE_FUNHOUSE)
  add_subdirectory(funhouse)
endif()
