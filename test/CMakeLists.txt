set (Boost_USE_STATIC_LIBS OFF) #enable dynamic linking

#search for unit_test_framework
find_package (Boost REQUIRED COMPONENTS unit_test_framework)

#create a ${EXEC_NAME} target from test.cpp
add_executable (${EXEC_NAME} tests.cpp)

#link Boost libraries to the new target
target_link_libraries (${EXEC_NAME} ${Boost_LIBRARIES})