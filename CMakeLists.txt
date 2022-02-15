# Copyright © SixtyFPS GmbH <info@sixtyfps.io>
# SPDX-License-Identifier: (GPL-3.0-only OR LicenseRef-SixtyFPS-commercial)

cmake_minimum_required(VERSION 3.14)
project(opengl_overlay_cpp LANGUAGES CXX)

list(PREPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

find_package(Slint REQUIRED)
find_package(OpenGLES2 REQUIRED)

add_executable(opengl_overlay main.cpp)
target_link_libraries(opengl_overlay PRIVATE Slint::Slint OpenGLES2::OpenGLES2)
slint_target_sources(opengl_overlay scene.slint)
