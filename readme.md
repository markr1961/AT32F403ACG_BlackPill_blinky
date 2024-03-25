## An Artery AT32F403A 'blinky' project in BlackPill dev board

A basic project using Artery AT32F403A CPU under IAR 7.80.4  
Project was created using Artery's code generation tool <- ?  

Because there is no support for this CPU under IAR 7.80.4 at this time, debug is limited to Cortex-M4 registers.

SysTick is running at 1mS, main loop at 10mS.

paths:
$PROJ_DIR$\..\..\libraries\drivers\inc
$PROJ_DIR$\..\..\libraries\cmsis\cm4\core_support
$PROJ_DIR$\..\..\libraries\cmsis\cm4\device_support
$PROJ_DIR$\..\inc

pre-defined symbols:
AT32F403ACGU7
USE_STDPERIPH_DRIVER
AT_START_F403A_V1