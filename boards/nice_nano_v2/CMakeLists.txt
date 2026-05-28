if(CONFIG_BOARD_NICE_NANO_V2)

board_runner_args(nrfjprog "--nrf-family=NRF52" "--softreset")
board_runner_args(jlink "--device=nrf52" "--speed=4000")
board_runner_args(openocd "--search=${NRF_BASE}/openocd")

include(${ZEPHYR_BASE}/boards/common/nrfjprog.board.cmake)
include(${ZEPHYR_BASE}/boards/common/jlink.board.cmake)
include(${ZEPHYR_BASE}/boards/common/openocd.board.cmake)

endif()
