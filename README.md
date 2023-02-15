# MADI

MADI is a development board based on various microcontroller chips but have the same form factor 21.59 mm x 30 mm. MADI comes with an open source [SDK](https://github.com/libmcu/madi). The SDK is designed so that you can focus on implementing your business logic without depending on the microcontroller type or platform.

So all of MADI family boards can be developed easily by one SDK. You can find a quick start guide [here](https://docs.libmcu.org/quickstart).

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
    <img width="500" alt="image" src="https://user-images.githubusercontent.com/20197999/218952542-a1177f72-08df-4d98-9c2b-1c9091225d1d.png">


## Pinout
<img width="1452" alt="image" src="https://user-images.githubusercontent.com/20197999/219049675-53acff68-352b-46b8-b291-0f53eb272fa5.png">


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
    | 12 |  |  |  |  |
    | 13 |  |  |  |  |
    | 14 |  |  |  |  |
    | 15 |  |  |  |  |
    | 16 |  |  |  |  |
    | 17 |  |  |  |  |
    | 18 |  |  |  |  |
    | 19 |  |  |  |  |
    | 20 |  |  |  |  |
    | 21 |  |  |  |  |
    | 22 |  |  |  |  |
 
- Pinout used internally
    |  | ESP32-S3 | nRF52840 | STM32G4 |
    | --- | --- | --- | --- |
    | GREEN LED | IO35 |  |  |
    | BQ25180 IRQ | IO14 |  |  |
    | BQ25180 SDA | IO17 |  |  |
    | BQ25180 SCL | IO18 |  |  |
    | EN_VBAT_MON | IO4 |  |  |
    | VBAT_MON | IO7 |  |  |
    | USER BUTTON | BOOT/IO0 |  |  |

## Design files

The full schematic, STEP 3D, drawings and CAD library can be found [here](https://github.com/libmcu/development-board).

### Schematic

### Mechanical Drawing

- PCB: 21.59 mm x 30 mm
- Thickness: 1.6mm

## Recommended operating conditions

Operating conditions for MADI are largely determined by recommended operating range specified in the electronic components used in MADI.

| Operating Temp Max. | 85 °C |
| Operating Temp Min. | -40 °C |
| VIN | 4.35 V ~ 5.5 V |
| VBAT | 2.2 V ~ 4.6 V |

## Power consumption

### Full-load

| MADI | VBUS_IN current @5V (mA) / Temperature (25 °C) | VBAT current @3.7V (mA) / Temperature (25 °C) |
| --- | --- | --- |
| #1 |  |  |
| #2 |  |  |
| #3 |  |  |
| Mean |  |  |

### Sleep mode

| MADI | VBUS_IN current @5V (mA) / Temperature (25 °C) | VBAT current @3.7V (mA) / Temperature (25 °C) |
| --- | --- | --- |
| #1 |  |  |
| #2 |  |  |
| #3 |  |  |
| Mean |  |  |
