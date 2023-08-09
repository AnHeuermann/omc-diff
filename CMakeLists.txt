cmake_minimum_required(VERSION 3.20)
project(omc-diff C)

find_package(FLEX REQUIRED)

FLEX_TARGET(omc_diff_lexer src/omc-diff.l ${CMAKE_CURRENT_BINARY_DIR}/lex.yy.c)
add_executable(omc-diff
  ${FLEX_omc_diff_lexer_OUTPUTS}
)

target_link_libraries(omc-diff ${FLEX_LIBRARIES})
install(TARGETS omc-diff
        RUNTIME_DEPENDENCIES
          DIRECTORIES ${FLEX_EXECUTABLE}
          PRE_EXCLUDE_REGEXES "api-ms-" "ext-ms-"
          POST_EXCLUDE_REGEXES "^\\/lib.*" "^\\/usr\\/lib.*" "^\\/usr\\/local\\/lib.*" ".*system32/.*\\.dll"
)
