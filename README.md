# RTK_GPS
A RTK GPS sensor Board for drones based around the Quectel LC29H Chip. It should offer accuracy of up to 5cm. It needs a Basestation or (depending on your country) position correcting GPS data that is send to the esp32.

For a more detailed write up you can check out the journal at [Blueprint](https://blueprint.hackclub.com/projects/7904).

## Why?
I made the project because I wanted to develop a drone and needed high precission and noticed that any available solutions are insanly expensive, so I came up with my own design.

## How?
I researched several different types of drone positioning systems and basically every professional use case uses RTK GPS due to its unmatched precission. I researched multiple RTK GPS modules and found none that were cheap enough/could do what I needed. So after a lot of researching I stumbled upon the quectel LC29H module that could everything I needed. It only needed some sort of correction data. I discovered that my country offers correction data via the internet so I just needed a way to serve this data to the modul over tha air. For that I decided to use an ESP32 as it already has native support for these kind of data transmissions by ardupilot. Because this arrangement needs some resistors and capacitors I designed my own Pcb.
<img width="1049" height="537" alt="grafik" src="https://github.com/user-attachments/assets/929d70f7-54ae-4459-8fa3-e274b161e9d6" />

<img width="1643" height="1030" alt="grafik" src="https://github.com/user-attachments/assets/1cd28b0f-52b1-4340-b6d7-598d745e404c" />

<img width="1687" height="1148" alt="grafik" src="https://github.com/user-attachments/assets/170a1775-b0cf-43ae-8073-6b1cf1b216fb" />

<img width="1481" height="1059" alt="grafik" src="https://github.com/user-attachments/assets/0e035bc0-d903-43b7-812d-cd2dc4912932" />

<img width="1633" height="1125" alt="grafik" src="https://github.com/user-attachments/assets/cdf9d5eb-1c3e-49cb-a9f7-8416b911a77e" />




| Designator     | Value                       | Footprint              |   Quantity |   Price | Link                                                         |   Total Price |
|:---------------|:----------------------------|:-----------------------|-----------:|--------:|:-------------------------------------------------------------|--------------:|
| C4, C5, C6     | 10uF                        | 603                    |          3 |    0.15 | JLCPCB Part                                                  |          0.45 |
| C7             | 100nF                       | 603                    |          1 |    0.05 | JLCPCB Part                                                  |          0.05 |
| D1             | LED                         | 603                    |          1 |    0.05 | JLCPCB Part                                                  |          0.05 |
| R1, R2, R5     | 10k                         | 603                    |          3 |    0.1  | JLCPCB Part                                                  |          0.3  |
| J5             | Conn_01x04_Socket           | PinHeader_1x04_P2.54mm |          1 |    0.2  | JLCPCB Part                                                  |          0.2  |
| SW1, SW2       | SW_Push                     | SW_SPST_B3S-1000       |          2 |    0.3  | JLCPCB Part                                                  |          0.6  |
| U1             | ESP32-WROOM-32E             | ESP32-WROOM-32E        |          1 |    3.5  | JLCPCB Part                                                  |          3.5  |
| U3             | AMS1117-3.3                 | SOT-223-3              |          1 |    0.25 | JLCPCB Part                                                  |          0.25 |
| GPS Antenna    | Helix Ceramic RTK Dual Band | External               |          1 |   13.59 | [Link](https://de.aliexpress.com/item/1005009918181431.html) |         13.59 |
| GPS Connector  | Generic Connector           | External               |          1 |    1.65 | [Link](https://de.aliexpress.com/item/1005005073187553.html) |          1.65 |
| Compass (U2?)  | QMC5583L                    | Module                 |          1 |    1.89 | [Link](https://de.aliexpress.com/item/1005006794324860.html) |          1.89 |
| ELRS Module    | Onboard Antenna             | Module                 |          1 |    7.69 | [Link](https://de.aliexpress.com/item/1005005236594556.html) |          7.69 |
| Cables AWG28   | Silicone Cable              | Wiring                 |          1 |    5.59 | [Link](https://de.aliexpress.com/item/1005007671008743.html) |          5.59 |
| Cables AWG24   | Silicone Cable              | Wiring                 |          1 |    7.89 | [Link](https://de.aliexpress.com/item/1005006350734418.html) |          7.89 |
| FC             | SpeedyBee F405 V3           | Fc                     |          1 |   39.39 | [Link](https://de.aliexpress.com/item/1005004868739263.html) |         39.39 |
| RTK GPS Module | Quectel LC29H (HDA)         | Module                 |          1 |   23.59 | [Link](https://de.aliexpress.com/item/1005006870751088.html) |         23.59 |
