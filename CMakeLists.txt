# Copyright © SixtyFPS GmbH <info@sixtyfps.io>
# SPDX-License-Identifier: (GPL-3.0-only OR LicenseRef-SixtyFPS-commercial)

cmake_minimum_required(VERSION 3.14)
project(opengl_overlay_cpp LANGUAGES CXX)

list(PREPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

find_package(SixtyFPS REQUIRED)
find_package(OpenGLES2 REQUIRED)

add_executable(opengl_overlay main.cpp)
target_link_libraries(opengl_overlay PRIVATE SixtyFPS::SixtyFPS OpenGLES2::OpenGLES2)
sixtyfps_target_60_sources(opengl_overlay scene.60)
