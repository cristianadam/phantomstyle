qt_add_executable(funhouse
  ColorTest.cpp
  FunHouse.cpp
  main.cpp
  MainWindow.cpp
  PhTestApp.cpp PhTestApp.h
  WidgetGallery.cpp WidgetGallery.h
  Profiling.h
)

target_link_libraries(funhouse PRIVATE PhantomStyle)
