cmake_minimum_required(VERSION 3.1...3.22)
project(Periodic_4_hyperbolic_triangulation_2_Tests)

find_package(CGAL REQUIRED QUIET OPTIONAL_COMPONENTS Core)
find_package(LEDA QUIET)

if((CGAL_Core_FOUND OR LEDA_FOUND))

  create_single_source_cgal_program("test_p4ht2_construct_point_2.cpp")
  create_single_source_cgal_program("test_p4ht2_exact_complex_numbers.cpp")
  create_single_source_cgal_program("test_p4ht2_intersections.cpp")
  create_single_source_cgal_program("test_p4ht2_locate.cpp")
  create_single_source_cgal_program("test_p4ht2_matrix.cpp")
  create_single_source_cgal_program("test_p4ht2_removal_iterator.cpp")
  create_single_source_cgal_program("test_p4ht2_removal.cpp")
  create_single_source_cgal_program("test_p4ht2_insert_degenerate.cpp")

else()

  message(
    STATUS
      "This program requires the CGAL library and the GMP library, and will not be compiled."
  )

endif()
