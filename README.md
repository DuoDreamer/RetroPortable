# RetroPortable
Portable Retro computer


2025-01-17 Initial Concept

Folding palmtop retro computer
  -Wide-format, similar to Atari Portfolio, HP LX Palmtop series, etc
  -CPU/electronics boards modular for different platform flavors
    -Should be carrier board with bus, serial, power modules independent of CPU Core?
    -Z80/180 core board with 512KB SRAM, Flash, TTL Serial output
    -6502 core board?
    -NES core board? Maybe NoaC with some LCD interface or converter? Could require KB with dpad/buttons like larger Rii units
    -Pi Pico 2 board
    -Provision for I2C bus for system control of Power, Battery, RTC?
  -OS:RomWBW, perhaps others
  -MicroSD slot for virtual disk drive emulation, SPI direct drive usage like RomWBW
  -Power:
    -14500 Lithium battery, 2x in parallel, feeding 5V boost and 3.3v converters for system, keyboard, LCD, speaker power
    -Idea: 2-slot 14500/AA battery bay with DPDT switch to use Lithium in parallel and AA in series.
    -5V/3.3V regulators, Lipo/LiFe charger, USB-C input for charge, maybe serial too. Solar charge controller with load-sharing like Adafruit board
    -Top clam shell surface having provision for lower power 6V solar panel for self-charging. Likely 0.5-1W panels based on available surface area
  -LCD Screen: wide or standard format LCD, with wide having space for speakers above/below screen, and standard format LCD having space for speakers left/right of screen
    -Screen either stand-alone Pico/ESP32-powered serial terminal, or maybe I/O-mapped low pin-count TMS style VDP.
    -Screen I/O to be 3.3v and 5V tolerant for different CPU core types?
  -Sound:
    -Sound modules? FPGA/Pico2 Multi-mode (AY,FM,SID,SN) emulated sound chip? Sound routed from CPU board to Stereo clamshell amp/speakers? Headphone jack?
  -Communications:
    -TTL Serial? USB-C charge/serial/microSD mount?
    -ESP32 FujiNet interface? Custom Fujinet target with same general network-ready features?
  -Keyboard: removable top panel for re-used Bluetooth/USB micro keyboards
    -Custom Keyboard module with Atari/HP style chicklet custom PCB and buttons?
    -Serial terminal keyboard handling? 8255-style bus I/O handling?
  -Body: likely Resin 3D Printed components
    -Top Flap: outer shell, LCD face
    -Base: body, CPU module inserts/standoffs, battery/CPU access panel, common frame keyboard holder
      -base cutouts for connector ports, TTL Serial,   maybe a GPIO panel with threaded inserts to attach various bus-tied external modules, maybe even RC2014-39/40 bus adapter
    
