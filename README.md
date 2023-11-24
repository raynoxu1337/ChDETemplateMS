# Template project for ChaDevelopmentEnvironment
This is the template project to build your c++ projects using ChaDevelopmentEnvironment. Just clone it or download a zip and use with CDE. 

## Usage
To build your C++ projects you need first configure with CMake, there is release configuration and debug configuration. After configure task is done, the build task can be run and you can then run your program. It is deffinitelly possible to expand the tasks to also have a clang build option, but there is no real need for that to be fair.

## CMakeLists.txt
You can edit the CMakeLists.txt to change the c/c++ standard. It by default includes all the sources in the directory so no need to thank me. When you add a package in vcpkg you will need to add whatever vcpkg tells you to paste into the CMakeLists.txt.
As an example you want to add "restclient-cpp" package. You would install it on VcPkg
> vcpkg install restclient-cpp

The VcPkg will tell you to add it to CMakeLists.txt using:
```find_package(restclient-cpp CONFIG REQUIRED)
 target_link_libraries(main PRIVATE restclient-cpp)
``````

So just paste it to your CMakeLists.txt and you can use it in your project, literally that simple, almost as easy as npm!

## VcPkg Tripplets
CDE uses default VCPKG tripplet of x64-mingw-static. The static version is used because its alot easier to distribute your built outputs, but if you want you can change the passed vcpkg tripplet in the tasks.json and launch.cmd in the CDE folder. Other logical tripplet that you could use is x64-mingw-dynamic.