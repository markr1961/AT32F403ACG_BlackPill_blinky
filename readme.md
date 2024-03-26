## A basic 'blinky' project for Artery AT32F403A on WeAct Studio BlackPill dev board

A simple project for Artery AT32F403A CPU in WeActStuio BlackPill.
compiles with IAR 7.80.4  
Project was created using Artery's code generation tool <- ?  
include all libraries and extensions (making it really huge!)  

SysTick is running at 1mS, main loop at 10mS.  

### (WeActStuio.BlackPill](https://github.com/WeActStudio/WeActStudio.BlackPill)
AT32F403ACGU7 240Mhz, RAM:96+128KB, ROM:256+768KB
WeAct Studio Official Links
- taobao: weactstudio.taobao.com
- aliexpress: weactstudio.aliexpress.com
- github: github.com/WeActTC
- gitee: gitee.com/WeAct-TC
- blog: www.weact-tc.cn

## pinout
PA0     User button  
PC13    Blue LED  
PA14    SWCLK  
PA13    SWDIO  

### USB-C
Data+   PA12  
Data-   PA11  

### SO-08 flash (W25QxxJVSSIQ)  
PA8     nCS  
PB1     CLK  
PB10    IO0/DI/MOSI  
PB11    IO1/DO/MISO  
PB7     IO2/nWP  
PB6     IO3/nReset  

### Clocks
PD0/PD1/HSE      8 MHz  
PC15/PC14/LSE   32 KHz  
VB      Vbat for RTC  
red     power LED  

### JTAG-20 debug connections
| pin |   JTAG  | dev board |  JP3  |  CPU  |
|-----|---------|---------- |-------|-------|
|  1  |  VTref  |   3.3V    |   1   |       |
|  7  |  SWDIO  |   SWDIO   |   2   |  PA13 |
|  9  |  SWClk  |   SWCLK   |   3   |  PA14 |
|  4  |   GND   |   GND     |   4   |       |
| 15  | nRESET  |   nRST    |   5   |       |

## Compiling on IAR 7.80.4

### paths
$PROJ_DIR$\..\..\libraries\drivers\inc
$PROJ_DIR$\..\..\libraries\cmsis\cm4\core_support
$PROJ_DIR$\..\..\libraries\cmsis\cm4\device_support
$PROJ_DIR$\..\inc

### pre-defined symbols
AT32F403ACGU7
USE_STDPERIPH_DRIVER
AT_START_F403A_V1

