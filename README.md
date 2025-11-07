# Firmware
## How write programm into microcontroller:

1. What microcontroller are on PCB ? 

| Controll PCB          | Microcontroller   |
| ----------------------| :---------------: |
| Baltica               | ---               |
| Boiler                | STM32             |
| Comfort               | STM32             |
| GSM                   | ---               |
| Mini                  | ---               |
| Push                  | ---               |
| Travel                | ---               |

2. Programming tool & software

| Microcontroller       | Programmator      | Link |
| ----------------------| :---------------: | ---- |
| STM32                 | ST-Link-V2        | https://www.st.com/en/development-tools/stm32cubeprog.html |
| Microchip             | ---               |       |
| Raspberry             | ---               |       |

3. Pinout for each PCB


### Baltica Controll Pinout
[Hex file with Baltica Heater code](./Baltica-Controll/Heater/PushBoil%20(85C).bin)

<img src="./Baltica-Controll/Heater/Baltica-Controll-Pinout.jpeg" width="400">





### Boiler Controll Pinout
[Hex file with Boiler Controll code](./Boiler-Controll/)

<img src="./Boiler-Controll/Comfort-Controll-STM32-Pinout.jpeg" width="400">



### Comfort-Controll Pinout

[Hex file with code](./Comfort-Controll/STM32_CC_V1.27.bin)

<img src="./Comfort-Controll/Comfort-Controll-STM32-Pinout.jpeg" width="400">




### GSM-AT0060-Modem Pinout

[Hex file with GSM-AT0060-Modem code]()

<img src="./TempImg.png" width="400">




### Mini-Controll Pinout

[Hex file with Mini-Controll code](./Mini-Controll/MiniControl.bin)

<img src="./Mini-Controll/MIni-Controll-Pinout.jpeg" width="400">




### Push-Controll Pinout

[Hex file with Push-Controll code]()

<img src="./TempImg.png" width="400">




### Travel-Box-Relay Pinout

[Hex file with Travel-Box code]()

<img src="./TempImg.png" width="400">


4. Programming HEX file

    4.1 STM32CubeProgrammer 