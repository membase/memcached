ADD_EXECUTABLE(cbcrypto_test
               cbcrypto_test.cc
               ${Memcached_SOURCE_DIR}/include/cbcrypto/cbcrypto.h)

TARGET_LINK_LIBRARIES(cbcrypto_test
                      cbcrypto
                      platform
                      cJSON
                      gtest gtest_main)

ADD_TEST(NAME cbcrypto-test
         WORKING_DIRECTORY ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}
         COMMAND cbcrypto_test)
