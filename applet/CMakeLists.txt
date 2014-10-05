
#set(kinum_SRCS
#      KinumApplet.cpp
#)

#kde4_add_plugin(plasma_applet_kinum ${kinum_SRCS})

#target_link_libraries(plasma_applet_kinum 
#    ${KDE4_PLASMA_LIBS}
#    ${KDE4_KDEUI_LIBS}
#    ${QT_QTDECLARATIVE_LIBRARY}
#)
 
#install(TARGETS plasma_applet_kinum
#        DESTINATION ${PLUGIN_INSTALL_DIR})
 
install(DIRECTORY package/
        DESTINATION ${DATA_INSTALL_DIR}/plasma/plasmoids/org.github.tmoschou.kinum)

install(FILES package/metadata.desktop
        DESTINATION ${SERVICES_INSTALL_DIR} RENAME plasma-applet-kinum.desktop)
        
#plasma_install_package(kinum org.github.tmoschou.kinum plasma/plasmoids applet)
