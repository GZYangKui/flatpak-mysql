cmake_minimum_required(VERSION 3.18)

project(flatpak_mysql C)

set(INSTALL_PREFIX app)
set(CMAKE_C_STANDARD 99)
set(MYSQL_CLIENT_VERSION 21.2.28)
set(CMAKE_PROJECT_DESCRIPTION "Wrap mysql office c language driver.")

aux_source_directory(. SOURCE_DIR)

install(DIRECTORY ./lib/ TYPE LIB)
install(DIRECTORY ./include/ TYPE INCLUDE)

configure_file(flatpak_mysql.pc.in lib/pkgconfig/flatpak_mysql.pc @ONLY)