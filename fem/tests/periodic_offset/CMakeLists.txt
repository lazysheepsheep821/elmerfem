INCLUDE(test_macros)
INCLUDE_DIRECTORIES(${CMAKE_BINARY_DIR}/fem/src)

CONFIGURE_FILE( test.sif test.sif COPYONLY)

file(COPY ELMERSOLVER_STARTINFO test.grd DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMER_TEST(periodic_offset)
ADD_ELMER_LABEL(periodic_offset quick)
