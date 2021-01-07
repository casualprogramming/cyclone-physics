
file(GLOB COMMON_DEMO_HEADERS
	${CMAKE_SOURCE_DIR}/src/demos/*.h
)

file(GLOB COMMON_DEMO_SOURCE
	${CMAKE_SOURCE_DIR}/src/demos/*.cpp
)

set(GLUT_INCLUDE_DIR "${CMAKE_SOURCE_DIR}/contrib/freeglut/include")
set(COMMON_DEMO_INCLUDE "${GLUT_INCLUDE_DIR}" "${CMAKE_SOURCE_DIR}/include" "${CMAKE_SOURCE_DIR}/src/demos")
set(COMMON_DEMO_LIBS ${GLUT_glut_LIBRARY} ${OPENGL_LIBRARIES})
link_directories(${CMAKE_SOURCE_DIR}/lib/win32/)

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