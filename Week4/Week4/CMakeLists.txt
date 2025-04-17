cmake_minimum_required(VERSION 3.15)

project(Week4Castle)

set(CMAKE_CXX_STANDARD 17)

add_definitions(-DUNICODE -D_UNICODE)

# Include Common and Week4 folders
include_directories("../../Common")
include_directories(".")

add_executable(Week4Castle WIN32
    Week4-6-ShapeComplete.cpp
    FrameResource.cpp              
    ../../Common/d3dUtil.cpp      
    ../../Common/d3dApp.cpp
    ../../Common/GeometryGenerator.cpp
    ../../Common/MathHelper.cpp
    ../../Common/GameTimer.cpp
)

target_link_libraries(Week4Castle
    d3d12
    dxgi
    dxguid
    d3dcompiler
    windowscodecs
)
