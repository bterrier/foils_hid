cmake_minimum_required(VERSION 3.5)

project(foils_hid LANGUAGES C)

set(SOURCES
  src/foils_hid.c
  src/rudp_hid_client.c
  )

add_library(foils_hid
    ${SOURCES}
    )
target_link_libraries(foils_hid PUBLIC rudp)
target_include_directories(foils_hid PUBLIC include)