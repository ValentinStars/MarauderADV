# M5Cardputer-Adv Port

This fork defaults to `MARAUDER_CARDPUTER_ADV` and keeps the original board
targets only as reference.

## Hardware Map

Display ST7789V2:
- CS `37`
- SCK `36`
- MOSI `35`
- DC `34`
- RST `33`
- BL `38`

Keyboard TCA8418:
- SDA `8`
- SCL `9`
- INT `11`

SD card SPI:
- CS `12`
- SCK `40`
- MISO `39`
- MOSI `14`

Other ADV peripherals:
- Battery ADC `10`
- NeoPixel `21`
- GPS UART TX `15`
- GPS UART RX `13`

## Local Build

PlatformIO now has a dedicated default environment:

```sh
pio run
```

The `advinfo` serial command and Device -> `ADV Status` screen print the most
important ADV runtime diagnostics.

The ADV PlatformIO profile uses a dedicated 8 MB partition table with two
3 MB OTA app slots and a SPIFFS data partition.
