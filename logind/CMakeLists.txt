add_executable(logind logind.c)
target_include_directories(logind PRIVATE ../md5/include)
target_link_libraries(logind
	$<TARGET_FILE:md5>
	$<TARGET_FILE:prs>
)
set_property(TARGET logind PROPERTY C_STANDARD 11)
