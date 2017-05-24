# add library
include_directories(
  .
  ../include
)
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_library(cv_bridge STATIC cv_bridge.cpp rgb_colors.cpp)
add_dependencies(cv_bridge ${catkin_EXPORTED_TARGETS})
target_link_libraries(cv_bridge ${OpenCV_LIBRARIES} ${catkin_LIBRARIES})
