add_executable(hello_bench hello_bench.cc)

target_link_libraries(hello_bench benchmark::benchmark)
