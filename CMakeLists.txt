cmake_minimum_required(VERSION 3.0)

project(fortran-csv-module LANGUAGES Fortran)

set(sources
  src/csv_kinds.f90
  src/csv_module.F90
  src/csv_parameters.f90
  src/csv_utilities.f90
)

add_library(csv ${sources})

add_executable(csv_test src/tests/csv_test.f90)
target_link_libraries(csv_test csv)
