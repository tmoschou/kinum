project(plasma-kinum)

#find_package(KDE4 REQUIRED)
find_package(KDE4 "4.9.0" REQUIRED)

include(KDE4Defaults)
  
add_definitions(
  ${QT_DEFINITIONS}
  ${KDE4_DEFINITIONS}
)

include_directories(
  ${CMAKE_SOURCE_DIR}
  ${CMAKE_BINARY_DIR}
  ${KDE4_INCLUDES}
)
 
add_subdirectory(applet)
add_subdirectory(dataengine)

#add_subdirectory(backends)
