# ESP32devreciever
An addon for my gamecube portable to enable wireless communications. The reciever will work for wireless gamecube controller(s) as well as wireless code upload for macros and inputs from a computer.

For the receiver, data integrity is vital for a solid wireless connection. I'd also like to be able to store macro files on the receiver, which should be activated by a hotkey or button combination. Connection should be seamless and integrated. Thankfully, no voltage regulators or power supplies are needed; however, to make flashing easier, I will incorporate a low level voltage regulator for the USB-C spec. On the portable itself, VIN will be supplied by the RVL-PMS-2, which has 3v3 out. ![image](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTUxNzgsInB1ciI6ImJsb2JfaWQifX0=--5f2e081f5eb896d7b6cfdf2ae53169af11307c2d/image.png)

This should take little to no space. Minimizing outputs(only 17IO and 1 PWM in) should only require a maximum of 20 pins, 10 on each side of the motherboard(including 1 for 3.3v and 1 for ground. No debug to minimize space requirements. I need to satisfy the IO requirements for most of these pins. ![image](/user-attachments/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTUxODAsInB1ciI6ImJsb2JfaWQifX0=--2266cf7e60c4a35060da9dc0a1a2a842ca5c00fb/image.png)

Utilizing the ESP32-WROOM-S3-N16 should be perfect; high flash memory, integrated SOC, and all the functionality of an ESP32. With that, I'll begin the schematic.

Finished developing the schematic, most components were brought over from the transmitter made earlier. Working from a new computer so I had to re download and modify footprint libraries. Smaller voltage regulator, limited my GPIO output pins severely so I could fit everything with just 20 jumper pins. PCB routing is going to be a pin, since I'll be using a 2layer board this time and need a much more compact PCB.<img width="1856" height="1252" alt="image" src="https://github.com/user-attachments/assets/8264c4a7-9fd3-4d94-92f7-5ffedbdba897" />

