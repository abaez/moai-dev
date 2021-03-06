cmake_minimum_required ( VERSION 2.8.5 )
project ( zlib )


set ( CMAKE_CURRENT_SOURCE_DIR "${MOAI_ROOT}/3rdparty/zlib-1.2.3/" )

set ( ZLIB_INCLUDES "${MOAI_ROOT}/3rdparty/zlib-1.2.3/" )

set ( ZLIB_SOURCES

  ${CMAKE_CURRENT_SOURCE_DIR}/adler32.c
  ${CMAKE_CURRENT_SOURCE_DIR}/compress.c
  ${CMAKE_CURRENT_SOURCE_DIR}/crc32.c
  ${CMAKE_CURRENT_SOURCE_DIR}/deflate.c
  ${CMAKE_CURRENT_SOURCE_DIR}/gzio.c
  ${CMAKE_CURRENT_SOURCE_DIR}/infback.c
  ${CMAKE_CURRENT_SOURCE_DIR}/inffast.c
  ${CMAKE_CURRENT_SOURCE_DIR}/inftrees.c
  ${CMAKE_CURRENT_SOURCE_DIR}/inflate.c
  ${CMAKE_CURRENT_SOURCE_DIR}/trees.c
  ${CMAKE_CURRENT_SOURCE_DIR}/uncompr.c
  ${CMAKE_CURRENT_SOURCE_DIR}/zutil.c

 )

add_library(zlib STATIC ${ZLIB_SOURCES})
target_include_directories(zlib PUBLIC ${ZLIB_INCLUDES})
set_target_properties( zlib PROPERTIES FOLDER Third-Party )