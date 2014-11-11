# Copyright (c) HBP 2014 Daniel.Nachbaur@epfl.ch
# Change this number when adding tests to force a CMake run: 2

set(TEST_LIBRARIES ${Boost_UNIT_TEST_FRAMEWORK_LIBRARY} zeq)
flatbuffers_generate_c_headers(FBS newEvent.fbs)
set_source_files_properties(newEvent.cpp PROPERTIES OBJECT_DEPENDS ${FBS_OUTPUTS})

include(CommonCTest)