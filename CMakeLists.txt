cmake_minimum_required (VERSION 3.11)
project(manchester_analyzer)

# custom CMake Modules are located in the cmake directory.
set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

include(ExternalAnalyzerSDK)

set(SOURCES 
src/ManchesterAnalyzer.cpp
src/ManchesterAnalyzer.h
src/ManchesterAnalyzerResults.cpp
src/ManchesterAnalyzerResults.h
src/ManchesterAnalyzerSettings.cpp
src/ManchesterAnalyzerSettings.h
src/ManchesterSimulationDataGenerator.cpp
src/ManchesterSimulationDataGenerator.h
)

add_analyzer_plugin(manchester_analyzer SOURCES ${SOURCES})
