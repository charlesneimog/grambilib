# Define your standard CMake header (for example):
cmake_minimum_required(VERSION 3.5)

set(PDCMAKE_DIR
    "${CMAKE_CURRENT_SOURCE_DIR}/resources/pd.cmake/"
    CACHE PATH "Path to pd.cmake")
include(${PDCMAKE_DIR}/pd.cmake)

project(grambilib~)

# ╭──────────────────────────────────────╮
# │          Object Definitions          │
# ╰──────────────────────────────────────╯
pd_add_external(grambidec~ src/grambidec.c)
pd_add_external(grambiman~ src/grambiman.c)
pd_add_external(grambipan~ src/grambipan.c)
