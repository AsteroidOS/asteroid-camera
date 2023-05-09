add_library(asteroid-camera main.cpp resources.qrc)
set_target_properties(asteroid-camera PROPERTIES PREFIX "")

target_link_libraries(asteroid-camera PUBLIC
	AsteroidApp)

install(TARGETS asteroid-camera
	DESTINATION ${CMAKE_INSTALL_LIBDIR})
