cmake_minimum_required(VERSION 3.15) 

set(PROJECT_NAME Lab)				 	 
project("${PROJECT_NAME}")


set(CMAKE_CXX_STANDARD 17)			 
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)


add_definitions(-DSFML_STATIC)		 
include_directories("inc/")
include_directories("ext/SFML/include/")	
link_directories("ext/SFML/lib/")	

add_executable("${PROJECT_NAME}" Lab1.cpp
)
											
target_link_libraries("${PROJECT_NAME}" sfml-graphics-s-d
						  sfml-window-s-d
						  sfml-system-s-d
						  opengl32
						  freetype
						  winmm
						  gdi32
						  sfml-audio-s-d
						  openal32
						  flac
						  vorbisenc
						  vorbisfile
						  vorbis
						  ogg)
file(COPY "times.ttf" DESTINATION "/")