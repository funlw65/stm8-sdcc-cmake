# STM8-SDCC-CMAKE

## About

This is project for developing applications for STM8 microcontrollers using SDCC compiler.

Project based on `https://github.com/ObKo/stm32-cmake`


There is support of STM8S and STM8L series at now.

Support of StdPeriph libraries will be added soon.

Required software:

* SDCC compiler - `http://sdcc.sourceforge.net/`
* CMake 2.8 or higher - `https://cmake.org/`
<!--* STM8 StdPeriph Library (optional)


You can found StdPeriph Libraries on `http://www.st.com`
STM8 StdPeriph Libraries Archives:

* `STM8016`  for STM8L15x/16x/05x
* `STM8012`  for STM8L10x
* `STM8069`  for STM8S
-->

## Usage

For successful build you need to define some variables.

* `CMAKE_TOOLCHAIN_FILE` - path to sdcc-generic.cmake toolchain file.
* `CMAKE_MODULE_PATH` - path to cmake files directory.
* `STM8_CHIP` - STM8 device name in lower or upper case, e.g. stm8l152c6
<!--* `STM8_StdPeriph_DIR` - path to std_periph directory-->


Example for makefiles:
	
	cmake -DCMAKE_TOOLCHAIN_FILE=<path_to_sdcc-generic.cmake> -DCMAKE_MODULE_PATH=<path_to_project_cmake_dir> -DSTM8_CHIP=<stm8_chip_definition> -G"MinGW Makefiles" <path_to_source_dir>


It builds sdcc's *.ihx file. If you need you can convert it to *.hex or *.bin file.