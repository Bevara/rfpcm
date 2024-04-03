cmake_minimum_required(VERSION 3.7)
project(Filters)

include(filters.cmake)

add_definitions(-fpic)

SET(RFPCM_SRC
        ${CMAKE_SOURCE_DIR}/reframe_rawpcm.c
        ${CMAKE_SOURCE_DIR}/bitstream.c
        ${CMAKE_SOURCE_DIR}/constants.c
)

SET(RFPCM_INC
        ${CMAKE_SOURCE_DIR}/include
)

add_filter(rfpcm
        "${RFPCM_SRC}"
        ""
        []
        ""
        "${RFPCM_INC}"
        ""
        "1")