cmake_minimum_required(VERSION 3.12)
include(pico_sdk_import.cmake)
project(mytest_project)
pico_sdk_init()

add_executable(mytest
	main.c
	)

pico_enable_stdio_usb(mytest 1)
pico_enable_stdio_uart(mytest 1)

pico_add_extra_outputs(mytest)
target_link_libraries(mytest pico_stdlib)


