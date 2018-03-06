set(SRC_DIR ${CMAKE_CURRENT_LIST_DIR})

set(SOURCES 
    ${SRC_DIR}/GoDialog.cpp
    ${SRC_DIR}/OpenGLView.cpp
    ${SRC_DIR}/SizeDialog.cpp
    ${SRC_DIR}/stdafx.cpp
    ${SRC_DIR}/yuvplayer.cpp
    ${SRC_DIR}/yuvplayerDlg.cpp)

set(HEADERS 
    ${SRC_DIR}/GoDialog.h
    ${SRC_DIR}/OpenGLView.h
    ${SRC_DIR}/pcre.h
    ${SRC_DIR}/resource.h
    ${SRC_DIR}/SizeDialog.h
    ${SRC_DIR}/stdafx.h
    ${SRC_DIR}/yuvplayer.h
    ${SRC_DIR}/yuvplayerDlg.h
)

set(RESOURCES
    ${SRC_DIR}/yuvplayer.rc
    ${SRC_DIR}/res/bitmap1.bmp
    ${SRC_DIR}/res/bitmap10.bmp
    ${SRC_DIR}/res/bitmap11.bmp
    ${SRC_DIR}/res/bitmap12.bmp
    ${SRC_DIR}/res/bitmap2.bmp
    ${SRC_DIR}/res/bitmap3.bmp
    ${SRC_DIR}/res/bitmap4.bmp
    ${SRC_DIR}/res/bitmap5.bmp
    ${SRC_DIR}/res/bitmap6.bmp
    ${SRC_DIR}/res/bitmap7.bmp
    ${SRC_DIR}/res/bitmap8.bmp
    ${SRC_DIR}/res/bitmap9.bmp
    ${SRC_DIR}/res/wi0111-32.ico
    ${SRC_DIR}/res/wi0111-48.ico
    ${SRC_DIR}/res/yuvplayer.rc2
)

add_definitions(-D_AFXDLL)
add_definitions(-D_CRT_SECURE_NO_WARNINGS)
set(CMAKE_MFC_FLAG 1)
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /UMBCS /D_UNICODE /DUNICODE")

add_executable(yuvplayer WIN32 ${SOURCES} ${HEADER} ${RESOURCES})
target_link_libraries(yuvplayer opengl32 glu32)
