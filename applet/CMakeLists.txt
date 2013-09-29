set(kinum_SRCS
      KinumApplet.cpp
)

kde4_add_plugin(plasma_applet_kinum ${kinum_SRCS})

target_link_libraries(plasma_applet_kinum 
                      ${KDE4_PLASMA_LIBS} ${KDE4_KDEUI_LIBS})
 
install(TARGETS plasma_applet_kinum
        DESTINATION ${PLUGIN_INSTALL_DIR})
 
install(FILES plasma-applet-kinum.desktop
        DESTINATION ${SERVICES_INSTALL_DIR})

install(DIRECTORY qml/
        DESTINATION ${DATA_INSTALL_DIR}/kinum/qml)

add_subdirectory(icons)
