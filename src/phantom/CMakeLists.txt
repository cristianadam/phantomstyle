qt_add_library(PhantomStyle STATIC
  phantomcolor.cpp phantomcolor.h
  phantomstyle.cpp phantomstyle.h
  phantomtweak.h
)

target_link_libraries(PhantomStyle
  PUBLIC
    Qt6::Core
    Qt6::Widgets
)

target_include_directories(PhantomStyle
  PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/..>
)

set_target_properties(PhantomStyle
  PROPERTIES POSITION_INDEPENDENT_CODE ON
)
