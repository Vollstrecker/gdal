add_gdal_driver(
  TARGET ogr_LIBKML2
  SOURCES libkml_headers.h
          ogrlibkmlfield.h
          ogr_libkml.h
          ogrlibkmlfeaturestyle.h
          ogrlibkmlfeature.h
          ogrlibkmlgeometry.h
          ogrlibkmlstyle.h
          ogrlibkmldriver.cpp
          ogrlibkmlfeaturestyle.cpp
          ogrlibkmllayer.cpp
          ogrlibkmlfeature.cpp
          ogrlibkmlgeometry.cpp
          ogrlibkmlstyle.cpp
          ogrlibkmldatasource.cpp
          ogrlibkmlfield.cpp
  CORE_SOURCES
          ogrlibkmldrivercore.cpp
  PLUGIN_CAPABLE
  NO_SHARED_SYMBOL_WITH_CORE
  NO_CXX_WFLAGS_EFFCXX
  NO_WFLAG_OLD_STYLE_CAST
)
if(NOT TARGET ogr_LIBKML2)
    return()
endif()

gdal_standard_includes(ogr_LIBKML2)
gdal_target_link_libraries(ogr_LIBKML2 PRIVATE LibKML::kmlbase)
