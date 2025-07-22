cmake_minimum_required(VERSION 3.8)
project(psm_tool)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

# Install directories
install(
  DIRECTORY urdf
  DESTINATION share/${PROJECT_NAME}
)
install(
  DIRECTORY launch
  DESTINATION share/${PROJECT_NAME}
)
install(
  DIRECTORY meshes
  DESTINATION share/${PROJECT_NAME}
)
# ADD THIS BLOCK to install your rviz config file
install(
  DIRECTORY config
  DESTINATION share/${PROJECT_NAME}
)
# The old rviz directory install can be removed if it's empty

ament_package()