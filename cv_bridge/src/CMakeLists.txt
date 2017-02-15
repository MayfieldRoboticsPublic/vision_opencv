# add library
include_directories(./)
add_library(cv_bridge STATIC cv_bridge.cpp rgb_colors.cpp)
add_dependencies(cv_bridge ${catkin_EXPORTED_TARGETS})
target_link_libraries(cv_bridge ${OpenCV_LIBRARIES} ${catkin_LIBRARIES})
