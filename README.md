# HK32F030MF4P6 Project Template 

* HSXP HK32F030M template project for GNU Arm Embedded Toolchain
* Supported programmers: J-Link, DAPLink/PyOCD, ST-LINK/PyOCD
* Supported IDE: VSCode

# HK32F030MF4P6

## Pinout - TSSOP20

| Pin | Func          | Pin | Func             |
| -- | -------------- | -- | ----------------- |
| 1  | PD4            | 20 | PD3 AIN3          |  
| 2  | PD5 AIN0 SWDIO | 19 | PD2 AIN4          |  
| 3  | PD6 AIN1       | 18 | PD1               |  
| 4  | NRST           | 17 | PC7               |  
| 5  | PA1 EXTCLK1    | 16 | PC6               |  
| 6  | PA2            | 15 | PC5 EXTCLK4       |  
| 7  | VSS VSSA       | 14 | PC4 AIN2 WKUP0    |  
| 8  | PD7 VCAP       | 13 | PC3               |  
| 9  | VDD VDDA       | 12 | PB4               |  
| 10 | PA3            | 11 | PB5 EXTCLK3 SWCLK |  

# File Structure

```
├── Build                       # Build results
├── Docs                        # Datasheet
├── Examples                    # Example code
├── flash.jlink                 # JLink download commander script
├── Libraries
│   ├── CMSIS
│   ├── Debug                   # SysTick delay and printf for debug
│   ├── FreeRTOS                # FreeRTOS library
│   ├── HK32F030M_Driver        # MCU peripheral driver
│   └── LDScripts
├── LICENSE
├── Makefile                    # Make config
├── Misc
│   └── vscode
├── README.md
├── rules.mk                    # Pre-defined rules include in Makefile 
└── User                        # User application code
└── Keil_User                   # Keil project Example

```

# Requirements

* Board using HK32F030MF4P6
* Programmer
  * J-Link: J-Link OB programmer
  * PyOCD: DAPLink, J-Link or ST-LINK
* SEGGER J-Link Software and Documentation pack [https://www.segger.com/downloads/jlink/](https://www.segger.com/downloads/jlink/)
* PyOCD [https://pyocd.io/](https://pyocd.io/)
* GNU Arm Embedded Toolchain

# Building

* Use Keil software for compiling the project.
* startup_hk32f030mf4p6.s file generate from CubeMx for stm32f030f4p6 and copy instead of original ones.
*  In the project options->Asm Tab-> Assembler Option, confirm that armclang was selected as compiler. 
