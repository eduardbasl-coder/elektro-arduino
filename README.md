# LCD Uptime Monitor

Jednoduchý Arduino projekt zobrazující
- systémový boot screen
- loading animaci
- uptime counter (doba běhu zařízení)
- status systému na 16x2 LCD displeji

Ideální jako
- mini fake server monitor
- homelab status panel
- desktop gadget
- základ pro embedded dashboard

---

# Preview

## Boot sekvence

```text
uptime 0s
status boot...
```

## Running režim

```text
uptime 154s
status running
```

---

# Features

- 25s bootloading sekvence
- animované tečky (`. .. ...`)
- realtime uptime counter
- kompatibilní s běžným 16x2 LCD
- jednoduchý Arduino UNO wiring
- low-resource projekt pro beginner embedded development

---

# Hardware

Použité komponenty

- Arduino UNO  Nano
- LCD 16x2 (HD44780 compatible)
- potenciometr 10kΩ (kontrast LCD)
- breadboard
- jumper wires

---

# Wiring

 LCD Pin  Arduino 
------
 RS  12 
 E   11 
 D4  5 
 D5  4 
 D6  3 
 D7  2 

Napájení
- VSS → GND
- VDD → 5V
- RW → GND

Kontrast
- VO → prostřední pin potenciometru

---

# Project Structure

```text
project
│
├── code
│   └── lcd_uptime.ino
│
├── schematic
│   └── schema.png
│
├── board
│   └── project.brd
│
├── media
│   ├── photo1.jpg
│   ├── photo2.jpg
│   └── demo.mp4
│
└── README.md
```

---

# Arduino Code

Hlavní funkce
- `millis()` → systémový timer
- boot delay → simulace startupu systému
- LCD output → status monitoring

Použité knihovny

```cpp
#include LiquidCrystal.h
```

---

# Upload

1. Otevři `.ino` soubor v Arduino IDE
2. Vyber správný COM port
3. Vyber desku
   - Arduino UNO
   - Arduino Nano
4. Klikni Upload

---

# Future Improvements

Možné upgrady

- RTC modul (Real Time Clock)
- CPURAM usage fake stats
- progress bar
- RGB backlight
- buzzer startup sound
- I2C LCD backpack
- teplota pomocí DHT22
- WiFi monitoring přes ESP8266ESP32

---

# Media

Do složky `media` přidej
- fotky zařízení
- video boot sekvence
- screenshoty schematu

---

# License

MIT License

Free to use, modify and share.

---

# Author

Created by Eduard Basl  
HomeLAB  Embedded  Arduino Project
