cmake_minimum_required(VERSION 3.6)

project(logind)

add_executable(logind login_server.c)
target_include_directories(logind PRIVATE ../md5/include)
target_link_libraries(logind $<TARGET_FILE:prs>)
set_property(TARGET logind PROPERTY C_STANDARD 11)
