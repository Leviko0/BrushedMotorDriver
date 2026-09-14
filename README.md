# BrushedMotorDriver

This driver board is designed for two 12V brushed motors based on an ESP32 and two DRV8245. It utilizes the NCV68261 for reverse current and reverse polarity protection and for power enable.

## Hardware overview

- **MCU:** ESP32-S3-WROOM-1
- **Motor drivers:** 2x TI DRV8245 (12V brushed DC motor driver)
- **Protection:** NCV68261 for reverse current/polarity protection and power enable, with DRVOFF fault handling
- **Power input:** XT60 connector for a 4S LiPo battery
- **Regulator:** TLV75533 LDO, 3.3V rail for the ESP32
- **Programming/data:** USB-C connector (USB 2.0)

## PCB design

- **4-layer stackup** with dedicated ground and power planes, to separate the ESP32's digital/RF signals from the motor drivers' switching noise
- **Thermal via arrays** under the DRV8245 exposed pads for heat dissipation
- **Ground stitching vias** to keep return paths low-impedance across the board
- **Trace widths scaled by current:** wider power traces for the motor outputs, standard-width traces for signal/logic


Schematic: <br />
<img width="754" height="793" alt="image" src="https://github.com/user-attachments/assets/f6bb485d-7016-4d02-aba1-9641d477df93" />

<br />

PCB: <br />
<img width="769" height="901" alt="image" src="https://github.com/user-attachments/assets/323915d6-56ff-4e8b-b5f9-6b31a791b78a" />





