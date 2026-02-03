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

