cmake_minimum_required (VERSION 2.8)

find_package(OpenGL REQUIRED)
find_package(GLUT)

if(MSVC AND (NOT GLUT_FOUND))
	find_library(GLUT glut
	    PATHS "${CMAKE_SOURCE_DIR}/lib" "${CMAKE_SOURCE_DIR}/lib/win32")

	find_library(GLUT32 glut32
	    PATHS "${CMAKE_SOURCE_DIR}/lib" "${CMAKE_SOURCE_DIR}/lib/win32")

	set(GLUT_LIBRARIES ${GLUT32} ${GLUT})
	message(${GLUT_LIBRARIES})
endif()

if(WIN32)
    set(PLATFORM_LIBRARIES winmm.lib)
endif()

file(GLOB COMMON_DEMO_HEADERS
	${CMAKE_SOURCE_DIR}/src/demos/*.h
)

file(GLOB COMMON_DEMO_SOURCE
	${CMAKE_SOURCE_DIR}/src/demos/*.cpp
)

set(COMMON_DEMO_INCLUDE "${CMAKE_SOURCE_DIR}/include" "${CMAKE_SOURCE_DIR}/src/demos")
set(COMMON_DEMO_LIBS ${GLUT_LIBRARIES} ${OPENGL_LIBRARIES} ${PLATFORM_LIBRARIES})

if(MSVC)
    set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /SAFESEH:NO")
endif()

add_subdirectory(ballistic)
add_subdirectory(bigballistic)
add_subdirectory(blob)
add_subdirectory(bridge)
add_subdirectory(explosion)
add_subdirectory(fireworks)
add_subdirectory(flightsim)
add_subdirectory(fracture)
add_subdirectory(platform)
add_subdirectory(ragdoll)
add_subdirectory(sailboat)