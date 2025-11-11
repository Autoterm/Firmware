# Firmware



## How programm microcontroller

1. <details>
    <summary> What microcontroller are on PCB </summary>

    | Controll PCB          | Microcontroller     |
    | ----------------------| :---------------:   |
    | Baltica               | STM32               |
    | Boiler                | STM32               |
    | Comfort               | STM32               |
    | GSM                   | STM32               |
    | Mini                  | STM32               |
    | Push                  | STM32               |
    | Travel Box            | STM32               |

</details>

2. <details>
    <summary> Selecting programming tool & software </summary>

    ### Programming software

    | Microcontroller       | Programmator      | Link |
    | ----------------------| :---------------: | ---- |
    | STM32                 | ST-Link-V2        | https://www.st.com/en/development-tools/stsw-link004.html |
    | Microchip             | PICkit4           | ----      |
    | Raspberry             | ---               | ----      |


    ### ST-Link-V2 Pinout
    
    <img src="./img/ST-Link-V2-Pinout.png" width="600">

</details>

3. <details>
    <summary> Pinout for each PCB </summary>

    +   <details>
        <summary> Baltica Controll Pinout </summary>

        [Hex file with Baltica Heater code](./Baltica-Controll/Heater/PushBoil%20(85C).bin)

        <img src="./Baltica-Controll/Heater/Baltica-Controll-Pinout.jpeg" width="400">
        </details>

    +   <details>
        <summary> Boiler Controll Pinout </summary>

        [Hex file with Boiler Controll code](./Boiler-Controll/)

        <img src="./Boiler-Controll/Comfort-Controll-STM32-Pinout.jpeg" width="400">
        </details>

    +   <details>
        <summary> Comfort Controll Pinout </summary>

        [Hex file with code](./Comfort-Controll/STM32_CC_V1.27.bin)

        <img src="./Comfort-Controll/Comfort-Controll-STM32-Pinout.jpeg" width="400">
        </details>

    +   <details>
        <summary> GSM-AT0060-Modem Pinout </summary>

        [Hex file with GSM-AT0060-Modem code](./GSM-AT0060-Modem/Qstar_4G_V1.24.bin)

        <img src="./img/TempImg.png" width="400">
        </details>

    +   <details>
        <summary> Mini Controll Pinout </summary>

        [Hex file with Mini-Controll code](./Mini-Controll/MiniControl.bin)

        <img src="./Mini-Controll/MIni-Controll-Pinout.jpeg" width="400">
        </details>

    +   <details>
        <summary> Push Controll Pinout </summary>

        [Hex file with Push-Controll code](./Push-Controll/PushControl_V1.00.bin)

        <img src="./Push-Controll/Push-Controll-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Travel-Box-Relay Pinout </summary>

        [Hex file with Travel-Box code](./Travel-Box-Relay/Pow_switch_V1.1.bin)

        <img src="./Travel-Box-Relay/Push-Controll-Pinout.jpeg" width="400">
        </details>


    </details>



4. <details>
    <summary> How to write HEX / Bin file into microcontroler </summary>
 
    +   <details>
        <summary> STM32 ST-LINK utility </summary>

        1. Download & install STM32 ST-LINK utility

        2. Open programm and connect ST Link v2 to PC

        3. Select from drop down menu Target -> Settings

        4. Configure programmator settings:

        <img src="./img/STLinkUtility1.png" width="400">

        5. Connect programming pins from ST Link V2 to programming pads on PCB. 
        > **_NOTE:_**  Keep holding programming pins.

        6. Press OK in Settings menu

        7. If connection successful you shoul see device memory map, family, ID.

        <img src="./img/STLinkUtility2.png" width="800">

        8. Select HEX / Bin file by clicling on File -> Open file -> *select file* -> Open. In logs you can see file checksum - we will need it to verify programm instalation.

        <img src="./img/STLinkUtility3.png" width="800">

        9. Select from upper menu Target -> Program & Verify. Double check file path and press *Start*.

        <img src="./img/STLinkUtility4.png" width="800">

        10. If programming succeed - compare programmed memory checksum with HEX / Bin file checksum.

        <img src="./img/STLinkUtility5.png" width="800">

        11. Disconnect from microcontroller by selcting Target -> Disconnect.
        > **_NOTE:_**  Now you can remove programming pins.

        </details> 

    +   <details>
        <summary> STM32CubeProgrammer </summary>

        1. Download & install STM32CubeProgrammer
    
        2. Open programm and connect ST Link v2 to PC

        3. Ensure that PC can read serial number and target voltage

        <img src="./img/prg1.png" width="1200">

        > **_NOTE:_**  Target voltage should be around +3.3V.

        4. Setup programming settings and connect to microcontroller

        <img src="./img/prg2.png" width="1200">

    </details>   

</details>    