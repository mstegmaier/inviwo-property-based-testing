#--------------------------------------------------------------------
# Inviwo PropertyBasedTesting Module
ivw_module(PropertyBasedTesting)

#--------------------------------------------------------------------
# Add header files
set(HEADER_FILES
    include/inviwo/propertybasedtesting/algorithm/coveringarray.h
    include/inviwo/propertybasedtesting/algorithm/generatingassignments.h
    include/inviwo/propertybasedtesting/algorithm/propertyanalyzing.h
    include/inviwo/propertybasedtesting/algorithm/reservoirsampling.h
    include/inviwo/propertybasedtesting/html/html.h
    include/inviwo/propertybasedtesting/html/report.h
    include/inviwo/propertybasedtesting/processors/faultycubeproxyprocessor.h
    include/inviwo/propertybasedtesting/processors/propertyanalyzer.h
    include/inviwo/propertybasedtesting/processors/imagecomparator.h
    include/inviwo/propertybasedtesting/processors/randomvolumegenerator.h
    include/inviwo/propertybasedtesting/propertybasedtestingmodule.h
    include/inviwo/propertybasedtesting/propertybasedtestingmoduledefine.h
    include/inviwo/propertybasedtesting/testproperty.h
)
ivw_group("Header Files" ${HEADER_FILES})

#--------------------------------------------------------------------
# Add source files
set(SOURCE_FILES
    src/algorithm/coveringarray.cpp
    src/algorithm/generatingassignments.cpp
    src/algorithm/propertyanalyzing.cpp
    src/algorithm/reservoirsampling.cpp
    src/html/html.cpp
    src/html/report.cpp
    src/processors/faultycubeproxyprocessor.cpp
    src/processors/propertyanalyzer.cpp
    src/processors/imagecomparator.cpp
    src/processors/randomvolumegenerator.cpp
    src/propertybasedtestingmodule.cpp
    src/testproperty.cpp
)
ivw_group("Source Files" ${SOURCE_FILES})

#--------------------------------------------------------------------
# Add shaders
set(SHADER_FILES
)
ivw_group("Shader Files" ${SHADER_FILES})

#--------------------------------------------------------------------
# Add Unittests
set(TEST_FILES
    tests/unittests/propertybasedtesting-unittest-main.cpp
)
ivw_add_unittest(${TEST_FILES})

#--------------------------------------------------------------------
# Create module
ivw_create_module(${SOURCE_FILES} ${HEADER_FILES} ${SHADER_FILES})

#--------------------------------------------------------------------
# Add shader directory to pack
# ivw_add_to_module_pack(${CMAKE_CURRENT_SOURCE_DIR}/glsl)
