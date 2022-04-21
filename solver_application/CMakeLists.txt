cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(solver)

add_executable(solver ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)

include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib
	${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib
)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib solver_lib)

target_link_libraries(solver
	PUBLIC formatter_ex
	PUBLIC solver_lib
)

install(TARGETS solver DESTINATION bin)

set(CPACK_PACKAGE_FILE_NAME "Solver")
set(CPACK_SOURCE_GENERATOR "TGZ;ZIP")
if(CPACK_GENERATOR_DEB)
	set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Dmitry")
	set(CPACK_GENERATOR "DEB")
endif()
if(CPACK_GENERATOR_RPM)
	set(CPACK_GENERATOR "RPM")
endif()
if(CPACK_GENERATOR_MSI)
	set(CPACK_GENERATOR "WIX")
endif()
if(CPACK_GENERATOR_DMG)
	set(CPACK_GENERATOR "DragNDrop")
endif()
include(CPack)