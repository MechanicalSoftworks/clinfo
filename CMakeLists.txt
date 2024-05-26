cmake_minimum_required(VERSION 3.25)

project(clinfo)

add_executable(clinfo src/clinfo.c)
target_include_directories(clinfo PUBLIC src)
target_include_directories(clinfo PUBLIC ${OpenCL_INCLUDE_DIRS})
target_link_libraries(clinfo OpenCL::OpenCL OpenCL::Headers ${CMAKE_DL_LIBS})

install(TARGETS clinfo RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}")
	
