INCLUDE(${CMAKE_CURRENT_SOURCE_DIR}/../test_macros.cmake)

CONFIGURE_FILE(ismip_coulomb.sif ismip_coulomb.sif COPYONLY)

FILE(COPY ELMERSOLVER_STARTINFO rectangle.grd DESTINATION "${CMAKE_CURRENT_BINARY_DIR}/")

ADD_ELMERICE_TEST(Friction_Coulomb)
ADD_ELMERICE_LABEL(Friction_Coulomb elmerice-fast)
