project(cyber-screen-brightness)
set(PROJECT_NAME cyber-screen-brightness)

set(SRCS
    main.cpp
)

add_executable(${PROJECT_NAME}
    ${SRCS}
)

target_link_libraries(${PROJECT_NAME}
        Qt5::Core
        Qt5::Gui
        Qt5::Widgets
)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION /usr/bin)
install(FILES org.cyber.brightness.pkexec.policy DESTINATION /usr/share/polkit-1/actions/)
