# Solar: Arduino synth for Eurorack, based on the Nebulophone

Solar is a synth with a keyboard of Cherry MX key switches. It uses an Arduino Nano. It is based on the [Nebulophone](https://bleeplabs.com/?p=2284) by Bleep Labs. You can use it in a Eurorack case or as a standalone synth.

![Solar](https://github.com/user-attachments/assets/0c9273e1-6546-44d8-835b-b5c3f02ac65d)

## Build guide and video

- Step-by-step build guide on Instructables: [Solar - Arduino Based Synth](https://www.instructables.com/Solar-Arduino-Based-Synth/)
- Video on YouTube: [Solar](https://www.youtube.com/watch?v=ggaYos6u02A)

## Features

- 8 waveforms
- Analogue low-pass filter, controlled by light (vactrol), with 5 LFO LED modes
- Correct tuning across 6 octaves
- Adjustable temperament and key
- 6 arpeggio modes with adjustable rate
- 2 sync inputs, to play with other synths

You do not have to sync Solar. You can also play it freely over the music of other synths.

## Changes from the Nebulophone

- I replaced the stylus keyboard with Cherry MX key switches.
- I designed a new PCB and a front panel. They fit in a Eurorack case.
- I added 2 sync inputs.

> **Note:** The sync inputs can need some adjustment, but after that they operate well.

## What you need

### Hardware

- All parts are in the [parts list](Solar%20-%20Parts%20List.pdf).
- The schematic is [schematic.png](schematic.png).
- The Gerber files for the PCB and the front panel are in [Gerber Files](Gerber%20Files/). You can send them to a PCB maker.
- Power: 9 V or 12 V, or a Eurorack power supply.

### Software

- Arduino IDE
- An Arduino Nano

You do not need to install libraries.

## Upload the firmware

1. Download this repository. Click **Code → Download ZIP**, then extract the ZIP file.
2. Open `Software/Solar - Arduino/Solar - Arduino.ino` in the Arduino IDE.
3. Connect the Arduino Nano to your computer with a USB cable.
4. In the **Tools** menu, set these values:
   - **Board:** Arduino Nano
   - **Processor:** ATmega328P
   - **Port:** the COM port of your Nano
5. Click **Upload**.
6. Wait for the message **Done uploading**.

> **Note:** If the upload fails, set **Processor** to **ATmega328P (Old Bootloader)**, then try again. Many clone Nano boards need this setting.

## How to play

The Instructables guide tells you how to play Solar.

## Files in this repository

| Folder or file | Contents |
|----------------|----------|
| `Software/Solar - Arduino/` | Firmware (Nebulophone code) |
| `Eagle Files/` | Eagle files for the PCB |
| `Front Panel Design/` | KiCad, Inkscape and image files for the front panel |
| `Gerber Files/` | Gerber files for the PCB and the front panel, ready to order |
| `Solar - Parts List.pdf` | Parts list |
| `schematic.png` | Schematic |

## Why I made it

I want to make my own modular synth that is simple to build. Each module has these aims:

- It operates from 9 V (and 12 V).
- It is easy to build, with a minimum of components.
- It uses an Arduino, to keep the parts count low and everything in tune.
- It fits in any Eurorack case, and it can use normal Eurorack power.
- It sounds good.

This was my first project with Cherry MX switches. They feel very good to play.

![Solar module](https://github.com/user-attachments/assets/1bae4e8f-a08e-4651-851d-24a50ec8612f)

## Credits

- Original synth design and code: the [Nebulophone](https://bleeplabs.com/?p=2284) by Dr. Bleep (John-Mike Reed), [Bleep Labs](https://bleeplabs.com/). Thank you, Bleep Labs.
- PCB, front panel, keyboard and sync inputs: Marcus ([lonesoulsurfer](https://github.com/lonesoulsurfer)).

## Support

Do you like this project? You can support my work on [GitHub Sponsors](https://github.com/sponsors/lonesoulsurfer).

## Licence

- **Hardware** (PCB, front panel and Gerber files): [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE). You can make, change and sell boards. If you share or sell a changed design, you must also share the changed design files under the same licence. Copyright (c) 2025 Marcus (lonesoulsurfer).
- **Firmware** (`Software/`): the Nebulophone code by Bleep Labs. Bleep Labs does not give a licence for this code. The CERN licence does **not** apply to it. Before you use the code for a commercial purpose, ask [Bleep Labs](https://bleeplabs.com/) for permission.
