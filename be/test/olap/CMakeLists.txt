# where to put generated libraries
set(LIBRARY_OUTPUT_PATH "${BUILD_DIR}/test/olap")

# where to put generated binaries
set(EXECUTABLE_OUTPUT_PATH "${BUILD_DIR}/test/olap")

ADD_BE_TEST(row_block_test)
ADD_BE_TEST(command_executor_test)
ADD_BE_TEST(bit_field_test)
ADD_BE_TEST(byte_buffer_test)
ADD_BE_TEST(run_length_byte_test)
ADD_BE_TEST(run_length_integer_test)
ADD_BE_TEST(stream_index_test)
ADD_BE_TEST(lru_cache_test)
ADD_BE_TEST(bloom_filter_test)
ADD_BE_TEST(bloom_filter_index_test)
ADD_BE_TEST(comparison_predicate_test)
ADD_BE_TEST(in_list_predicate_test)
ADD_BE_TEST(null_predicate_test)
ADD_BE_TEST(file_helper_test)
ADD_BE_TEST(file_utils_test)
ADD_BE_TEST(delete_handler_test)
ADD_BE_TEST(column_reader_test)
ADD_BE_TEST(row_cursor_test)

## deleted
# ADD_BE_TEST(olap_reader_test)
# ADD_BE_TEST(vectorized_olap_reader_test)
