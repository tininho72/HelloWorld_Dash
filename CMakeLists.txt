cmake_minimum_required (VERSION "3.8")

project ("HelloWorld_Dash")

add_executable("${PROJECT_NAME}" "Main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin)		#${CMAKE_INSTALL_PREFIX}/bin
install(FILES "Main.cpp" DESTINATION src)		        #${CMAKE_INSTALL_PREFIX}/src

include (CTest)
add_test("Test_I" ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME})
#add_test("Test_II" ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME} "Parameter1")

