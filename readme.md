## A basic 'blinky' project for Artery AT32F403A on WeAct Studio BlackPill dev board

[Home on git](https://github.com/markr1961/AT32F403ACG_BlackPill_blinky.git)  

A simple project for Artery AT32F403A CPU on WeActStuio BlackPill.  
compiles with IAR 7.80.4  
Project was created using Artery's code generation tool <- ?  
include all libraries and extensions (making it really huge!)  

## Compiling on IAR 7.80.4
SysTick is running at 1mS, main loop at 10mS.  

### paths
$PROJ_DIR$\..\..\libraries\drivers\inc  
$PROJ_DIR$\..\..\libraries\cmsis\cm4\core_support  
$PROJ_DIR$\..\..\libraries\cmsis\cm4\device_support  
$PROJ_DIR$\..\inc  

### pre-defined symbols
AT32F403ACGU7  
USE_STDPERIPH_DRIVER  
AT_START_F403A_V1  

### [WeActStuio.BlackPill](https://github.com/WeActStudio/WeActStudio.BlackPill)
AT32F403ACGU7: 240Mhz,RAM:96+128KB,ROM:256+768KB Timer x 14,SysTick x 1,RTC x 1,I2C x 3,SPI x 4,UART x 7,SDIO x 1,USBFS x 1,CAN x 2 ...
[Artery Official website](www.arterytek.com/en/)

#### WeAct Studio Official Links
taobao: www.weactstudio.taobao.com  
aliexpress: www.weactstudio.aliexpress.com  
github: www.github.com/WeActTC  
gitee: www.gitee.com/WeAct-TC  
blog: www.weact-tc.cn  

## pinout
PA0     User button     BUTTON_PIN  
PC13    Blue LED        LED_PIN  
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
