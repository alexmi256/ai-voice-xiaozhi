# What
Documenting a XiaoZhi AI chatbot PCB that's sold on Aliexpress and other places for pretty cheap ($9USD)

# Why
The board sold comes with XiaoZhi AI but apparently the seller has access to all interactions.
Flashing the board with self built XiaoZhi would be the best outcome.

# Notes
This [XiaoZhi discussion](https://github.com/78/xiaozhi-esp32/discussions/1371) has some good starting info.

LCD appears to be JD9853

## Dumping Firmware
You don't need to do any pin grounding to access info via esptool.
Just plug in via USB. Only the green light will be on.
```
(venv) [alex@um780real esptool]$ esptool --chip esp32s3 --port /dev/ttyACM0 flash-id
esptool v5.1.0
Connected to ESP32-S3 on /dev/ttyACM0:
Chip type:          ESP32-S3 (QFN56) (revision v0.2)
Features:           Wi-Fi, BT 5 (LE), Dual Core + LP Core, 240MHz, Embedded PSRAM 2MB (AP_3v3)
Crystal frequency:  40MHz
USB mode:           USB-Serial/JTAG
MAC:                28:37:2f:f8:44:70

Stub flasher running.

Flash Memory Information:
=========================
Manufacturer: 68
Device: 4018
Detected flash size: 16MB
Flash type set in eFuse: quad (4 data lines)
Flash voltage set by eFuse: 3.3V
```

# Resources
- [AI Robot Voice Companion for All Age Emotional Interaction Companion Chat Robot Long Battery Life Gifts Chatbot AI GPT Deepseek](https://www.aliexpress.com/item/1005009935602461.html)
- https://github.com/78/xiaozhi-esp32
- https://github.com/Mo7d748/xiaozhi-esp32
- https://docs.espressif.com/projects/esptool/en/latest/esp32/installation.html
- https://github.com/78/xiaozhi-esp32/discussions/1371
- https://cloud.binary.ninja/bn/9a777727-d246-4de8-88c6-ff30a6774708
- https://documentation.espressif.com/esp32-s3_datasheet_en.pdf
- https://www.facebook.com/groups/HomeAssistant/posts/4152498265021512 initial post where I found info about board. Lot's of complaining from OP unfortunately. Also found PCB image without TF card.

# TODO
- [x] Dump firmware
- [ ] Look at partition tables
- [ ] Find secrests
