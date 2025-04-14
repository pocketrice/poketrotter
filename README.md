# pokétrotter
A modern take on the [Pokéwalker](https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9walker) as an overambitious and overextended amateur embedded/hacking project.

![pokewalker promo banner](https://github.com/user-attachments/assets/9ca4a41e-3c97-4b78-a153-1fbf118176b6)

> Presently (optimistically!!) planned is as follows. The aim is for no hardware modification, minimal implementation cost (both monetary and utility), and simple constructive usage. If the project ends up unflatteringly eviscerated, at least I will have learned a bit of hardware design (ᵕ—ᴗ—)

- SLOT1 = either **original ROM HGSS (OROM)** or **modified ROM flashcart (MROM)**.
  - Enables potential for a Pokéwalker-like mod for BW/BW2!
  - **OROM** = IR, **MROM** = Wi-Fi & SLOT2 peripheral

- Independently powered SLOT2 "magic box"
  - Likely Sparkfun ESP8266 + IR TX/RX board + 64KiB FRAM.
  - GBA-compliant form factor and FRAM read/write pins
    - In a sense, more of a "GBA lookalike" than an actual cart
  - If MROM, 2-way IR comms just like OROM!
    - SLOT1 takes care of just reading/writing to SLOT2 à la Pal Park. The latter runs on its own power and independently does all TX/RX operations!
  - 802.11b WAP?
    - May scrap depending on feasibility (e.g. no SLOT2 writing, power risk)
      - ...but also neat benefits and upkeep redundancy.
    - Can use native DS WFC interface!
      - Potential expansion as an effortless local Nintendo WFC WAP
      - Download Play, PictoChat, etc.
    - Easy data read/write for modern devices.
      - Good alternative for avoiding potential console damage or no need for dedicated peripheral (e.g. DeSmuME extension).
  - Independent and detachable
    - Constructive use as general-purpose IR-to-WiFi converter, such as backing up Pokéwalker data
    - Intermediate data bank if needed (e.g. safety backups, transferring between PTOK! devices, extra features like a "PC" system, data-limited MBCs)
    - This way any mods are isolated and never touch original hardware!
   
- . ݁₊ ⊹ _**PTOK!**_ . ݁˖ . ݁
  - A fun way to say, "_OK for Pokétrotter!_" (or _"Pokétalk!"_)
    - Companion to the "Nintendo Seal of Quality"
  - Any device that can interface with the Pokétrotter system, 99% likely thru that magic SLOT2 box. (IR? Wi-Fi?)
  - _Biiiiig_ stretch is for interconnectivity (trading!)
  - Enables easier implementations such as, say, on a pedometer!
 
- Game Boy Color
  - Has native IR TX/RX!
  - Either MBC3000 v4 or microcontroller-based MBC7 clone with Bosch BMA150-minimum accuracy accessor OR MBC7 donor flashcart
  - Ideally a custom Pokéwalker-like ROM built from the ground up with more features — Gen 5 dex, unique cries, Pokeáthlon...
    - Original had 2KB RAM/48KB ROM
    - MBC3000 has 64-128KB FRAM + 4-8MB ROM (depends on MBC3 vs MBC5 mode & RTC toggle)
    - MBC7 has 256B EEPROM + <2-16MB(?) ROM
  - Colo(u)r support!!!
  - Great for OTG — sunlit TFT and lovely pixel density!
 
- Other devices
  - Display/controller shield + case
    - Refit the SLOT2 magic box as an 'authentic' Pokéwalker!
    - ...amazing opportunity to tack a CIB and manuals for it and call it a "Pokétrotter"...!
  - Pebble/Core Time
    - Friendly hackable UI, visual flair, and easy on the eyes!
  - Desktop/mobile emulators (OpenEmu, Delta, Lemuroid...)
    - Trivial given already making MROMs. Modern and mobile!!

> To the reader, please accept this malformed diagram at your convenience and leisure.

_...feasibility is a problem for tomorrow. Surely nothing will go wrong ~! •ᴗ•_
