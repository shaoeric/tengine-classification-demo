cmake_minimum_required(VERSION 3.19)
project(tengine_demo)

add_executable(tengine_demo ./main.cpp src/tengine_operations.c)

# 包含目录
include_directories(${PROJECT_SOURCE_DIR}/include)

#link_directories(${PROJECT_SOURCE_DIR}/lib)

# 导入库文件
set(tengine-lib ${PROJECT_SOURCE_DIR}/lib/tengine-lite.lib
        ${PROJECT_SOURCE_DIR}/lib/tengine-lite.dll)
target_link_libraries(${PROJECT_NAME} ${tengine-lib})