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
<img width="500" alt="image" src="https://user-images.githubusercontent.com/20197999/219046405-8cde11a0-d9e8-427d-b304-b0ab0f981c44.png"><img width="500" alt="image" src="https://user-images.githubusercontent.com/20197999/219046447-2c5f6d1f-e041-4928-9530-d69c596b9965.png"><img width="500" alt="image" src="https://user-images.githubusercontent.com/20197999/219046476-6b640449-048e-4393-982f-7bee86d5b960.png">


- 2 x 11 Header pin pinout
    | No. | ESP32-S3 | nRF52840 | STM32G4 | Note |
    | --- | --- | --- | --- | --- |
    | 1 |  |  |  |  |
    | 2 |  |  |  |  |
    | 3 |  |  |  |  |
    | 4 |  |  |  |  |
    | 5 |  |  |  |  |
    | 6 |  |  |  |  |
    | 7 |  |  |  |  |
    | 8 |  |  |  |  |
    | 9 |  |  |  |  |
    | 10 |  |  |  |  |
    | 11 |  |  |  |  |

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

| Operating Temp Max.  | 85 °C |
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
