project(local_unibreak C)

cmake_minimum_required(VERSION 3.4)

set(LIBUNIBREAK_SOURCE_DIR "${PROJECT_SOURCE_DIR}/../../../../thirdparty/${REPO_LIBUNIBREAK_SRCDIR}/src")

include_directories(${LIBUNIBREAK_SOURCE_DIR})

set(LIBUNIBREAK_SOURCE
	${LIBUNIBREAK_SOURCE_DIR}/unibreakbase.c
	${LIBUNIBREAK_SOURCE_DIR}/unibreakdef.c
	${LIBUNIBREAK_SOURCE_DIR}/linebreak.c
	${LIBUNIBREAK_SOURCE_DIR}/linebreakdata.c
	${LIBUNIBREAK_SOURCE_DIR}/linebreakdef.c
	${LIBUNIBREAK_SOURCE_DIR}/emojidef.c
	${LIBUNIBREAK_SOURCE_DIR}/graphemebreak.c
	${LIBUNIBREAK_SOURCE_DIR}/wordbreak.c
)

add_library(local_unibreak STATIC ${LIBUNIBREAK_SOURCE})
