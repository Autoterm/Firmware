# Firmware

## How to programm microControler in heater

<details>
    <summary>Air 2D</summary>

</details>

<details>
    <summary>Air 4D</summary>

</details>

<details>
    <summary>Air 9D</summary>

</details>


<details>
    <summary>Flow 5</summary>

</details>

<details>
    <summary>Flow 14</summary>

</details>


## How programm microControler in Control uint

1. <details>
    <summary> Which microControler is on PCB </summary>

    | Control PCB          | MicroControler     |
    | ----------------------| :---------------:   |
    | Baltica               | STM32               |
    | Boiler                | STM32               |
    | Comfort               | STM32               |
    | GSM                   | STM32               |
    | Mini                  | STM32               |
    | Push                  | STM32               |
    | Travel Box            | STM32               |
    | CAN Gateway           | STM32               |
</details>

2. <details>
    <summary> Selecting programming tool & software </summary>

    ### Programming software

    | MicroControler       | Programmator      | Link |
    | ----------------------| :---------------: | ---- |
    | STM32                 | ST-Link-V2        | https://www.st.com/en/development-tools/stsw-link004.html |
    | STM32                 | STLINK-V3MINIE    | https://www.st.com/en/development-tools/stm32cubeprog.html |
    | Microchip             | PICkit4           | ----      |
    | Raspberry             | ---               | ----      |


    ### ST-Link-V2 Pinout
    
    <img src="./img/ST-Link-V2-Pinout.png" width="600">

    ### STLINK-V3MINIE

    <img src="./img/ST-Link-V3-Mini-Pinout.png" width="600">

</details>


3. <details>
    <summary> Pinout for each PCB </summary>

    +   <details>
        <summary> Baltica Control Pinout </summary>

        [Hex file with Baltica Heater code](./Baltica-Control/Heater/PushBoil%20(85C).bin)

        <img src="./Baltica-Control/Control Panel/Comfort Control/Comfort-Control-STM32-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Boiler Control Pinout </summary>

        [Hex file with Boiler Control code](./Boiler-Control/)

        <img src="./Boiler-Control/Comfort-Controll-STM32-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Comfort Control Pinout </summary>

        [Hex file with code](./Comfort-Control/STM32_CC_V1.27.bin)

        <img src="./Comfort-Control/Comfort-Control-STM32-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> GSM-AT0060-Modem Pinout </summary>

        [Hex file with GSM-AT0060-Modem code](./GSM-AT0060-Modem/Qstar_4G_V1.24.bin)

        <img src="./GSM-AT0060-Modem/GSM-Modem-STM32-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Mini Control Pinout </summary>

        [Hex file with Mini-Control code](./Mini-Control/MiniControl.bin)

        <img src="./Mini-Control/MIni-Control-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Push Control Pinout </summary>

        [Hex file with Push-Control code](./Push-Control/PushControl_V1.00.bin)

        <img src="./Push-Control/Push-Control-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> Travel-Box-Relay Pinout </summary>

        [Hex file with Travel-Box code](./Travel-Box-Relay/Pow_switch_V1.1.bin)

        <img src="./Travel-Box-Relay/Push-Control-Pinout.jpeg" width="600">
        </details>

    +   <details>
        <summary> CAN Gateway Pinout </summary>

        [Hex file with CAN Gateway code](./CAN-Gateway/UART-CAN-GATEWAY_V1.01.hex)

        <img src="./CAN-Gateway/CAN-Gateway-Pinout.jpeg" width="600">
        </details>    


</details>



4. <details>
    <summary> How to write HEX / Bin file into microcontroler </summary>
 
    +   <details>
        <summary> STM32 ST-LINK utility ( Only for ST-Link/v2)</summary>
        
        4.1. Download & install STM32 ST-LINK utility

        4.2. Open programm and connect ST Link v2 to PC

        4.3. Select from drop down menu Target -> Settings

        4.4. Configure programmator settings:

        <img src="./img/STLinkUtility1.png" width="400">

        4.5. Connect programming pins from ST Link V2 to programming pads on PCB.  
        > **_NOTE:_**  Keep holding programming pins.

        4.6. Press OK in Settings menu

        4.7. If connection successful you shoul see device memory map, family, ID.

        <img src="./img/STLinkUtility2.png" width="800">

        4.8. Select HEX / Bin file by clicling on File -> Open file -> *select file* -> Open. In logs you can see file checksum - we will need it to verify programm instalation.

        <img src="./img/STLinkUtility3.png" width="800">

        4.9. Select from upper menu Target -> Program & Verify. Double check file path and press *Start*.

        <img src="./img/STLinkUtility4.png" width="800">

        4.10. If programming succeed - compare programmed memory checksum with HEX / Bin file checksum.

        <img src="./img/STLinkUtility5.png" width="800">

        4.11. Disconnect from microControler by selcting Target -> Disconnect.
        > **_NOTE:_**  Now you can remove programming pins.

        </details> 

    +   <details>
        <summary> STM32CubeProgrammer </summary>

        4.1. Download & install STM32CubeProgrammer.
        
        4.2. Open programm and connect ST-Link-V3-Minie to PC.
        
        4.3. Ensure that PC can read serial number and target voltage.

        <img src="./img/prg1.png" width="1200">

        > **_NOTE:_**  Target voltage should be around +3.3V.

        4.4. Click on second icon from left side menu to open programming tab and enter path to file.

        <img src="./img/prg2.png" width="1200">

        4.5. Setup programming settings and connect programming *pins* from ST-Link to programming *pads* on PCB. Press connect.

        <img src="./img/prg3.png" width="1200">

        > **_NOTE:_**  Keep holding programming pins.

        4.6. If connection was successful you should see information about MCU eg. Device name, Type, ID...

        <img src="./img/prg4.png" width="1200">

        4.7. Press *Start Programming*

        <img src="./img/prg5.png" width="1200">

        4.8 Press *Disconnect* and remove programming pins
    </details>   

5. <details>
    <summary> Potenial problems & how to fix them </summary>

    Programmator can not connect to target
    - Check swDIO and swCLK pins
    - Check GND connection
    - Check if programmator can read Target voltage ( around +3.3V )
    - Select other option from ST-LINK conguration->Shared ( Enabled / Disabled ) 

    Programmator can not erase memory
    - Change mode to Normal 
    - Select lower frequency ( 5 - 200 ) kHz 


</details>    