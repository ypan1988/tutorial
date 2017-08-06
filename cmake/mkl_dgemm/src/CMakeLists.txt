INCLUDE_DIRECTORIES(/opt/intel/mkl/include)
LINK_DIRECTORIES(/opt/intel/mkl/lib/intel64 /opt/intel/lib/intel64)

ADD_EXECUTABLE(main dgemm_example.cc)
TARGET_LINK_LIBRARIES(main mkl_intel_lp64 mkl_intel_thread mkl_core iomp5 pthread m dl)
