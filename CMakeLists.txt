cmake_minimum_required(VERSION "3.15.4")

project("HelloWorld")

add_executable("${PROJECT_NAME}" "Main.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin) #${CMAKE_INSTALL_PREFIX}/bin
install(FILES "Main.cpp" DESTINATION src)          #${CMAKE_INSTALL_PREFIX}/src

include(CTest)

add_test("test1" "${MAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}")
 