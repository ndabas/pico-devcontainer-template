cmake_minimum_required(VERSION 3.13)

# initialize the SDK based on PICO_SDK_PATH
# note: this must happen before project()
include(pico_sdk_import.cmake)

project(pico-vcpkg-ce-example)

# initialize the Raspberry Pi Pico SDK
pico_sdk_init()

add_executable(pico-vcpkg-ce-example
    hello.c
)

# Add pico_stdlib library which aggregates commonly used features
target_link_libraries(pico-vcpkg-ce-example pico_stdlib)

# create map/bin/hex/uf2 file in addition to ELF.
pico_add_extra_outputs(pico-vcpkg-ce-example)
