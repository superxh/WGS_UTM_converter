cmake_minimum_required(VERSION 2.8.3)
project(GeoHeader)

set(SOURCES

		${CMAKE_CURRENT_SOURCE_DIR}/src/MGRS.cpp
		${CMAKE_CURRENT_SOURCE_DIR}/src/PolarStereographic.cpp
		${CMAKE_CURRENT_SOURCE_DIR}/src/TransverseMercator.cpp
		${CMAKE_CURRENT_SOURCE_DIR}/src/Utility.cpp
		${CMAKE_CURRENT_SOURCE_DIR}/src/UTMUPS.cpp
		${CMAKE_CURRENT_SOURCE_DIR}/src/Math.cpp

		)
set(HEADERS

		${CMAKE_CURRENT_SOURCE_DIR}/include/Constants.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/MGRS.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/PolarStereographic.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/TransverseMercator.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/Utility.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/UTMUPS.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/Math.hpp
		${CMAKE_CURRENT_SOURCE_DIR}/include/Config.h

		)
add_library(GEOH ${SOURCES} ${HEADERS})

include_directories(include include)

add_executable(main main.cpp ${HEADERS} ${SOURCES})

set( CMAKE_EXPORT_COMPILE_COMMANDS ON )
