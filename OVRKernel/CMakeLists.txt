cmake_minimum_required( VERSION 3.6.0 )

project ( fontue )

set( PATHNAME "./core" )

add_subdirectory( ${PATHNAME} vrs-core )

add_executable( fontue 
	main.cpp 
)

target_include_directories( fontue PRIVATE 
	${PATHNAME}
	${PATHNAME}/Android 
	${PATHNAME}/Kernel 
)

target_link_libraries( fontue PRIVATE 
	vrs-core 
)