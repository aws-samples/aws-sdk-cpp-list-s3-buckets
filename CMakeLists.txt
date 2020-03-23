cmake_minimum_required(VERSION 3.2)
project(list-s3-buckets)

option(BUILD_SHARED_LIBS "Build shared libraries" ON)

find_package(AWSSDK REQUIRED COMPONENTS s3)
add_executable(list-s3-buckets main.cpp)

target_compile_features(list-s3-buckets PUBLIC cxx_std_11)
target_link_libraries(list-s3-buckets ${AWSSDK_LINK_LIBRARIES})
