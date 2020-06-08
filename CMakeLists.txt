CMAKE_MINIMUM_REQUIRED(VERSION 3.16)
PROJECT(NPCAP LANGUAGES C)

add_definitions(-D_WINDLL)
add_library(PACKET_LIB "")

target_sources(PACKET_LIB
    PRIVATE
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//AdInfo.cpp
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//netcfgapi.cpp
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//Packet32.cpp
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//ProtInstall.cpp
        ${CMAKE_SOURCE_DIR}//packetWin7//npf//npf//win_bpf_filter.c
    PUBLIC
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//debug.h
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//netcfgapi.h
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//Packet32-Int.h
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//ProtInstall.h
        ${CMAKE_SOURCE_DIR}//packetWin7//Dll//strsafe.h
        )



