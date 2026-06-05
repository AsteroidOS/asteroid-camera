add_library(asteroid-camera main.cpp)
set_target_properties(asteroid-camera PROPERTIES PREFIX "")

asteroid_app_qml_module(asteroid-camera
	main.qml
)

target_link_libraries(
	asteroid-camera
	PUBLIC
		Asteroid::AsteroidApp6
)

install(
	TARGETS asteroid-camera
	DESTINATION ${CMAKE_INSTALL_LIBDIR}
)
