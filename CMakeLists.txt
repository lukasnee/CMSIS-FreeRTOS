add_library(cmsis_freertos INTERFACE)

target_sources(
  cmsis_freertos
  PRIVATE CMSIS/RTOS2/FreeRTOS/Source/cmsis_os2.c
)

target_include_directories(cmsis_freertos INTERFACE CMSIS/RTOS2/FreeRTOS/Include)

target_link_libraries(cmsis_freertos INTERFACE freertos_kernel)