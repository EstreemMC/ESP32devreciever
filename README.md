# ESP32devreciever
An addon for my gamecube portable to enable wireless communications. The reciever will work for wireless gamecube controller(s) as well as wireless code upload for macros and inputs from a computer.

For the receiver, data integrity is vital for a solid wireless connection. I'd also like to be able to store macro files on the receiver, which should be activated by a hotkey or button combination. Connection should be seamless and integrated. Thankfully, no voltage regulators or power supplies are needed; however, to make flashing easier, I will incorporate a low level voltage regulator for the USB-C spec. On the portable itself, VIN will be supplied by the RVL-PMS-2, which has 3v3 out.<img width="1675" height="1055" alt="image" src="https://github.com/user-attachments/assets/626c0b4a-bf86-44db-b2db-581cd0bda3a4" />


This should take little to no space. Minimizing outputs(only 17IO and 1 PWM in) should only require a maximum of 20 pins, 10 on each side of the motherboard(including 1 for 3.3v and 1 for ground. No debug to minimize space requirements. I need to satisfy the IO requirements for most of these pins. <img width="790" height="799" alt="image-1" src="https://github.com/user-attachments/assets/60966495-632b-403b-b86f-5c25ec408aeb" />


Utilizing the ESP32-WROOM-S3-N16 should be perfect; high flash memory, integrated SOC, and all the functionality of an ESP32. With that, I'll begin the schematic.

Finished developing the schematic, most components were brought over from the transmitter made earlier. Working from a new computer so I had to re download and modify footprint libraries. Smaller voltage regulator, limited my GPIO output pins severely so I could fit everything with just 20 jumper pins. PCB routing is going to be a pin, since I'll be using a 2layer board this time and need a much more compact PCB.<img width="1856" height="1252" alt="image" src="https://github.com/user-attachments/assets/8264c4a7-9fd3-4d94-92f7-5ffedbdba897" />

For some reason, this PCB layout and routing was infinitely more difficult than my last. I can attribute most of the difficulties to the dramatically smaller size and the lack of 4 layers, with me settling for just two. overall, I'm really happy with the way it turned out and I can't wait to implement it on my actual console!

<img width="882" height="695" alt="image" src="https://github.com/user-attachments/assets/da93efe0-6d5d-4f3f-a463-d75a8e22c91c" />

<img width="733" height="473" alt="image" src="https://github.com/user-attachments/assets/95996574-539d-4f93-b249-d8098cad69e1" />

<img width="649" height="458" alt="image" src="https://github.com/user-attachments/assets/fd5a0094-a009-4e74-8a7c-18ba53bbf586" />
