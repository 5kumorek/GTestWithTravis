cmake_minimum_required(VERSION 3.5.1)

# Zarzadaj wyszukania i dolaczenia papietua GTest
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})
# Dolacz sciezke ${GTEST_INCLUDE_DIRS} do INCLUDE_PATH

add_executable(PalindromeTest PalindromeTest.cpp)
target_link_libraries(PalindromeTest ${GTEST_BOTH_LIBRARIES} palindromeLib pthread)
add_test(PalindromeTest PalindromeTest)
# Zarejestruj stworzony test
