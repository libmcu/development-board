# MADI

MADI is a development board based on various microcontroller chips but have the same form factor 21.59 mm x 30 mm. MADI comes with an open source [SDK](https://github.com/libmcu/madi). The SDK is designed so that you can focus on implementing your business logic without depending on the microcontroller type or platform. So all of MADI family boards can be developed easily by one SDK. You can find a quick start guide [here](https://docs.libmcu.org/quickstart).

[Main documentation of the MADI can be found here!](https://docs.libmcu.org/boards/libmcu.html)

## Overview
![image](https://user-images.githubusercontent.com/20197999/218473752-cf4155c1-084b-4cd4-ba1b-d018b4e2ab4f.png)

- ESP32-S3 / nRF52840 / STM32G4 are supported currently
- TI’s advanced battery management IC (BQ25180) and fully supported driver
- GPIO pin access through 2 x 11 pin headers with edge castellations
    - 2 x ADC / 1 x I2C / 1 x SPI / 1 x UART
    - Can be surface mounted as a module
- External Quad-SPI Flash with eXecute In Place (XIP) (for nRF52840 and STM32G4)
- ARM Serial Wire Debug (SWD) by USB C-type port
- Green LED, User button and Reset button
- 4-layer PCB design that mean better signal integrity and power integrity than other open-source development boards.
        <img width="500" alt="4-layer" src="https://user-images.githubusercontent.com/20197999/218952542-a1177f72-08df-4d98-9c2b-1c9091225d1d.png">


## Pinout
<img width="1500" alt="pinout" src="https://user-images.githubusercontent.com/20197999/219062569-9bd5deb6-e02e-45cc-be36-fe252628cdd2.png">



- 2 x 11 Header pin pinout
    | No. | ESP32-S3 | nRF52840 | STM32G4 | Note |
    | --- | --- | --- | --- | --- |
    | 1 | 3V3 | 3V3 | 3V3 | 3.3V LDO output |
    | 2 | GND | GND | GND |  |
    | 3 | IO35 | P0.20 | PA15 |  |
    | 4 | IO36 | P0.22 | PA5 |  |
    | 5 | IO1 | P0.04 | PA0 | ADC1 |
    | 6 | IO2 | P0.05 | PA3 | ADC2 |
    | 7 | IO37 | P0.19 | PC11 |  |
    | 8 | IO38 | P0.21 | PA1 |  |
    | 9 | GND | GND | GND |  |
    | 10 | IO43 | P0.23 | PA2 | UART_TX |
    | 11 | IO44 | P0.25 | PB4 | UART_RX |

    | No. | ESP32-S3 | nRF52840 | STM32G4 | Note |
    | --- | --- | --- | --- | --- |
    | 22 | VIN | VIN | VIN | External power input |
    | 21 | VSYS | VSYS | VSYS | BQ25180 System Output |
    | 20 | GND | GND | GND |  |
    | 19 | VBAT | VBAT | VBAT | Battery Connection |
    | 18 | GND | GND | GND |  |
    | 17 | IO13 | P0.29 | PB14 | SPI_MISO |
    | 16 | IO12 | P0.28 | PB13 | SPI_CLK |
    | 15 | IO11 | P0.03 | PB15 | SPI_MOSI |
    | 14 | IO10 | P1.15 | PB12 | SPI_nCS |
    | 13 | IO17 | P1.13 | PA8 | I2C_SDA |
    | 12 | IO18 | P1.12 | PA9 | I2C_SCL |
 
- Pinout used internally
    | Function | ESP32-S3 | nRF52840 | STM32G4 |
    | --- | --- | --- | --- |
    | GREEN LED | IO35 | P0.20 | PA15 |
    | BQ25180 IRQ | IO14 | P0.26 | PC6 |
    | BQ25180 SDA | IO17 | P1.13 | PA8 |
    | BQ25180 SCL | IO18 | P1.12 | PA9 |
    | EN_VBAT_MON | IO4 | P0.27 | PB2 |
    | VBAT_MON | IO7 | P0.31 | PC4 |
    | USER BUTTON | IO0 | P1.07 | PB8 |

## Recommended operating conditions

Operating conditions for MADI are largely determined by operating range specified in the electronic components used in MADI.
    | Parameter | Value |
    | --- | --- |
    | Operating Temp Max. | 85 °C |
    | Operating Temp Min. | -40 °C |
    | VIN | 4.35 V ~ 5.5 V |
    | VBAT | 2.2 V ~ 4.6 V |

## Support libmcu

Please consider supporting libmcu by buying some of products from:

https://k32175.wixsite.com/libmcu

## Contact us

[Slack](https://libmcu.slack.com/)
