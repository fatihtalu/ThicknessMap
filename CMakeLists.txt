cmake_minimum_required(VERSION 3.13.4)

project(ThicknessMap)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/fatihtalu/Slicer-ThicknessMap#readme")
set(EXTENSION_CATEGORY "Shape Analysis")
set(EXTENSION_CONTRIBUTORS "Muhammed Fatih Talu (Inonu University)")
set(EXTENSION_DESCRIPTION "Calculation bone thickness mapping")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/fatihtalu/Slicer-ThicknessMap/main/ThicknessMap.png")
set(EXTENSION_SCREENSHOTURLS "")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ThicknessMap)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
