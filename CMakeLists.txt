CMAKE_MINIMUM_REQUIRED(VERSION 3.16)
PROJECT(NPCAP LANGUAGES C)

add_definitions(-D_WINDLL)
add_library(PACKET_LIB "")

target_sources(PACKET_LIB
    PRIVATE
        packetWin7/Dll/AdInfo.cpp
        packetWin7/Dll/netcfgapi.cpp
        packetWin7/Dll/Packet32.cpp
        packetWin7/Dll/ProtInstall.cpp
        packetWin7/npf/npf/win_bpf_filter.c
    PUBLIC
        packetWin7/Dll/debug.h
        packetWin7/Dll/netcfgapi.h
        packetWin7/Dll/Packet32-Int.h
        packetWin7/Dll/ProtInstall.h
        packetWin7/Dll/strsafe.h
        )



