cmake_minimum_required(VERSION 3.6.0)

project(asteroid-camera
	VERSION 0.0.1
	DESCRIPTION "Default camera app for AsteroidOS")

find_package(AsteroidApp REQUIRED)

set(CMAKE_MODULE_PATH ${ASTEROID_MODULE_PATH})

include(FeatureSummary)
include(GNUInstallDirs)
include(AsteroidCMakeSettings)
include(AsteroidTranslations)

find_package(Qt5 COMPONENTS Multimedia REQUIRED)

add_subdirectory(src)

generate_desktop(${CMAKE_SOURCE_DIR} asteroid-camera)

feature_summary(WHAT ALL FATAL_ON_MISSING_REQUIRED_PACKAGES)
