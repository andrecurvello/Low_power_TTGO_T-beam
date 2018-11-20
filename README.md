# Low power TTGO T-beam 

The TTGO T-beam is a microcontrollers with a ESP32, WiFi, Bluetooth, GPS, LORA and Battery handling. Therefore it is especially suitable for off grid applications. However, little documentation can be found on reducting battery consumption.

This sketch demonstates how battery consumption can be reduced to 10ma during sleep, see image below. Please feel free to push more power reduction methods.

<table class="image">
<caption align="bottom">TTGO T-Beam 10ma power comsumption</caption>
<tr><td><img src="https://joep.space/img/ttgo_t-beam_power-consumption_2.jpg" width="250" alt="TTGO T-Beam 10ma power comsumption"/></td></tr>
</table>

## Components
| Chip        | Application   | Documentation                                                            | Power reduction methods  |
| ----------- |-------------  | ------------                                                             |-------                   |
| Esp 32      | Processor     | <https://docs.espressif.com/projects/esp-idf/en/latest/>                 | Deep sleep               |
| -           |      -        |                           -                                              | Power-down of RTC peripherals and memories  |
| -           |      -        |                           -                                              | GPIO isolation            |
| -           |      -        |                           -                                              | LED 14 low                |
| Neo-6m      | GPS           | <https://www.u-blox.com/en/product/neo-6-series>                         | Power Save Mode           |
| SX1276      | Lora          | <https://www.semtech.com/products/wireless-rf/lora-transceivers/SX1276>  | Sleep mode                | 
| CP2104      | USN to UART bridge | <https://www.silabs.com/products/interface/usb-bridges/classic-usb-bridges/device.cp2104> | TODO/not possible |
| w25q32 | Flash memory       | <https://www.winbond.com/resource-files/w25q32jv%20dtr%20revf%2002242017.pdf> | TODO/not possible |
| tp5400 | Battery management | <http://www.tpwic.com/index.php?m=content&c=index&a=show&catid=172&id=71> | TODO/not possible |
| 4a2d   | Voltage regulator  | <https://www.st.com/resource/en/datasheet/ld3985.pdf> | TODO/not possible |


## Dependencies
* esp32 Arduino core: <https://github.com/espressif/arduino-esp32>
* Arduino LoRa: <https://github.com/sandeepmistry/arduino-LoRa>
## Useful links
* Official Github: <http://github.com/LilyGO/TTGO-T-Beam>
* TTGO T-beam wiki: <http://ttgobbs.com>
