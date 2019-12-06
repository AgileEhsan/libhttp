cmake_minimum_required(VERSION 2.8.9)
project (libhttp)

#Bring the headers, such as Student.h into the project
include_directories(include)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.c")

#Generate the shared library from the sources
add_library(libhttp SHARED ${SOURCES})

#add_executable(src/testmime.c)