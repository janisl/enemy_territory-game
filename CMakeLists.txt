project(rtcw_sp-game)

cmake_minimum_required(VERSION 2.6)
if(COMMAND cmake_policy)
	cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -pipe -fmessage-length=0 -fvisibility=hidden")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -D_DEBUG")
set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -Winline -ffast-math -fomit-frame-pointer -finline-functions -fschedule-insns2")

include(CheckTypeSize)
check_type_size(void*  SIZEOF_VOID_PTR)

if(${SIZEOF_VOID_PTR} MATCHES "8")
	set(ARCH "x86_64")
else()
	set(ARCH "i386")
	set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -mcpu=i686 -march=i686")
endif()
message(STATUS "Using platform suffix ${ARCH}")

set(LIBRARY_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(src)
