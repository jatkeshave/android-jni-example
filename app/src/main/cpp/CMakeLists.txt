cmake_minimum_required(VERSION 3.18)

project("jniexamples")
add_library(jniexamples SHARED)
find_library(ANDROID_LOG REQUIRED log)
target_sources(jniexamples
        PRIVATE
        jniexamples.cpp
        )
target_link_libraries(jniexamples
        PRIVATE
        ${ANDROID_LOG}
        )
