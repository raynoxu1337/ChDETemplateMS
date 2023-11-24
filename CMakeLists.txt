cmake_minimum_required (VERSION 3.12)

project(ChaDETemplate)

file(GLOB sources CONFIGURE_DEPENDS "*.h" "*.cpp")

add_executable(main ${sources})

#Example of where to put the package includes, copy these from "vcpkg install packagename" output!
#find_package(restclient-cpp CONFIG REQUIRED)
#target_link_libraries(main PRIVATE restclient-cpp)
  