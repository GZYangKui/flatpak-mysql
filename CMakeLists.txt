cmake_minimum_required(VERSION 3.0)

project(mysql-client C)

set(CMAKE_C_STANDARD 99)

aux_source_directory(. SOURCE_DIR)

install(DIRECTORY ./lib/ TYPE LIB)
install(DIRECTORY ./include/ TYPE INCLUDE)

install(FILES mysqlclient.pc DESTINATION pkgconfig/)