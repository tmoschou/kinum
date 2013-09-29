set(kinum_engine_SRCS
      KinumEngine.cpp
)

kde4_add_plugin(plasma_engine_kinum ${kinum_engine_SRCS})

target_link_libraries(plasma_engine_kinum
#    ${KDE4_KDECORE_LIBS}
    ${KDE4_PLASMA_LIBS}
#    ${KDE4_KIO_LIBS}
#    QtNetworkManager
)

install(TARGETS plasma_engine_kinum
        DESTINATION ${PLUGIN_INSTALL_DIR})

install(FILES plasma-engine-kinum.desktop
        DESTINATION ${SERVICES_INSTALL_DIR})
