![image](https://github.com/mytechnotalent/dc540-0x00001/blob/main/DC540%20Angels%20Of%20Death.png?raw=true)

# dc540-0x00002
DC540 hacking challenge 0x00002 [MicroPython CTF].

<br>

## PROMOTIONAL VIDEO - WATCH NOW [HERE](https://youtu.be/YJAa4o7WXkE) ON YOUTUBE

<br>

## Prior Challenge [HERE](https://github.com/mytechnotalent/dc540-0x00001)

<br>

## Join DC540 Discord [HERE](https://discord.gg/TC9V9RCr5U)

<br>

## FREE Reverse Engineering For All Self-Study Course [HERE](https://github.com/mytechnotalent/Reverse-Engineering-Tutorial)

<br>

## Parts
[Raspberry Pi Pico](https://www.canakit.com/raspberry-pi-pico.html?cid=usd&src=raspberrypi)<br>
[Set of 2 x 20-pin Headers for Raspberry Pi Pico](https://www.canakit.com/set-of-2-20-pin-headers-for-raspberry-pi-pico.html)<br>
[830 Hole Breadboard](https://www.canakit.com/solderless-breadboard-830-hole.html)<br>
[Jumper Wires Male to Male - Pack of 30](https://www.canakit.com/jumper-wires-male-to-male-6.html)<br>
[20 Pcs 6 mm 2 Pin Momentary Tactile Tact Push Button Switch Through Hole Breadboard](https://www.amazon.com/Momentary-Tactile-Through-Breadboard-Friendly/dp/B07WF76VHT)
[Micro USB Cable High Speed Data and Charging, Nylon Braided Charger Cord, 3-Pack, 3 Feet](https://www.amazon.com/Rankie-Micro-Charging-Braided-3-Pack/dp/B01JPDTZXK)<br>

## Schematic
![image]()

<br>

## BRIEF
The SEAL Team 8 message has been successfully decoded, and we have learned that the entire “Dark Eyes” physical infrastructure is designed solely with MicroPython. The specific hardware of choice is the Raspberry Pi Pico microcontroller which contains the frozen MicroPython bytecode within the .elf and .uf2 firmware images that Dr. Rinn and her team have developed.

Natalia Agapov, a “Dark Eyes” Infrastructure Engineer, sympathetic to the extensive damage the SolarWinds hacks have done around the world captured a screen-shot of a collection of hand-written post-it notes outside Dr. Rinn's private study on her burner phone. She then obtained and copied the bc0.h, firmware.elf and firmware.uf2 files to a usb drive which was the specific firmware for 1337 Gate from Dr. Rinn's laptop.

She then went directly to the one and only way in or out of the elaborate compound which is located at Gate 1337. She escaped the "Dark Eyes" underground compound and managed to make her way to Vladivostok, Russia by means of the Trans-Siberian Railway. Along the way she came across the Internet-Magazin where she found a hardwired laptop inside an abandoned building and downloaded the Tor Browser. She navigated to http://emailondeck.com  where she created a temporary e-mail address and reached out to the "Five Eyes" HQ, Pine Gap, in Alice Springs, Australia sharing her physical coordinates in the hopes she might be rescued out of Russia. Her goal was simple:  hand off her burner phone with the image and her usb drive containing the .elf and .uf2 firmware of the 1337 Gate firmware.
Upon receiving the coordinates from Natalia at “Five Eyes” HQ, Bets Fielding was tasked with sneaking on board the DBS Cruise Ferry which was now used for cargo shipments after the Covid pandemic. Her mission was to find Natalia and bring her safely back to Sakaiminato, Japan where she would get her a new identity with the help of the allied forces.

It was hard to leave Natalia in Japan, but Bets knew it was what Natalia wanted. Bets asked Natalia to reach out if she ever needed anything again, and left Natalia for the long journey home to Northern Virginia.

When Bets arrived back home, she and her team met in their newly constructed classified field office to begin reverse engineering the .elf binary. They successfully extracted the capture.png containing Natalia's screenshot of Dr. Rinn's hand-written notes in addition to a copy of the Gate 1337 firmware in both .elf and .uf2 formats as well as a bc0.h file, but they were unsure of its purpose.

They flashed the .uf2 on a Raspberry Pi Pico to see how specifically the firmware operated and ran an unsuccessful string analysis as all of the relevant strings were encrypted with the world's most advanced encryption referred to as the Rinn Encryption.

The team cloned the latest Radare2 repo and built from source at https://github.com/radareorg/radare2. They used an Ubuntu distro. First they ran `radare2 -w arm -b 16 firmware.elf`. Then they ran `aaaa` and began to search the strings by typing `iz ~..` However, they found no usable strings. They made some changes to the MicroPython bytecode, ran `elf2uf2 firmware.elf firmware.uf2`, and finally flashed the .uf2 to the Pico. To date they have not been able to crack the 1337 Gate password and are struggling to find next steps.

Bets also reviewed the QSTR MicroPython Documentation to get familiar with how MicroPython handled strings located at  https://docs.micropython.org/en/latest/develop/qstr.html.

<br>

## MISSION
You have been selected by the DC540 ANGELS OF DEATH to be the Reverse Engineer on this mission. Your task is to review the attached capture.png and bc0.h to find clues of where to begin reverse engineering the .elf binary. Your mission is to hack the MicroPython bytecode and use the elf2uf2 conversion utility to get the entrance flag and report back to, "The Assassin" with your results by sending a private Discord DM to Bets Fielding.

## HINT
"Sometimes it is good to have a Russian translator."

<br>

## License
[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
