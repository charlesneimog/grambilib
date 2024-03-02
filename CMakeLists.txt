# Define your standard CMake header (for example):
cmake_minimum_required(VERSION 3.5)
include(${CMAKE_CURRENT_SOURCE_DIR}/resources/pd.build/pd.cmake) # pd.build
project(grambilib)

#╭──────────────────────────────────────╮
#│          Object Definitions          │
#╰──────────────────────────────────────╯
set_pd_external_path(${CMAKE_CURRENT_SOURCE_DIR}/${project_name})
add_pd_external(grambidec_tilde grambidec~ src/grambidec.c)
add_pd_external(grambiman_tilde grambiman~ src/grambiman.c)
add_pd_external(grambopac_tilde grambipan~ src/grambipan.c)

# ──────────────────────────────────────

target_compile_options(grambidec_tilde PRIVATE "-O3" "-Wall" "-Wshadow" "-ffast-math" "-funroll-loops" "-fomit-frame-pointer" "-mfpmath=sse" "-msse" "-msse2" "-msse3")


