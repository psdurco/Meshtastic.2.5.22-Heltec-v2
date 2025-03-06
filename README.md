# Meshtastic 2.5.22 for Heltec V2

This repository provides the compiled firmware for **Meshtastic 2.5.22** for the **Heltec V2** board, since the official Meshtastic Flasher tool currently only supports **Heltec V3**.

## 📌 Available Files

The following files are included in this repository:

- `bootloader.bin`
- `firmware.bin`
- `firmware.elf`
- `firmware.factory.bin`
- `partitions.bin`
- `meshtastic-heltec-v2-2.5.22.zip` (all files in a single package)

## 🚀 Flashing Instructions

There are two options for flashing the firmware onto your **Heltec V2**: using the **Meshtastic Web Flasher** or the **ESP Web Flasher**. Before proceeding, you must **put your Heltec V2 into programming mode**.

### **🔧 Putting Heltec V2 into Programming Mode**
1. **Connect the Heltec V2 to your computer via USB**.
2. **Hold the "PRG" (Program) button** on the board.
3. **While holding "PRG", press and release the "RST" (Reset) button**.
4. **Release the "PRG" button**.
5. The device is now in **bootloader mode** and ready to be flashed.

### **Option 1: Using the Meshtastic Web Flasher**
1. Go to **[Meshtastic Web Flasher](https://flasher.meshtastic.org/)**.
2. Click on **"Upload your own firmware release zip or bin"**.
3. Select `firmware.bin` from the provided files.
4. Ensure your **Heltec V2 is in programming mode** (see instructions above).
5. Click **"Flash"** and wait for the process to complete.
6. Once done, reboot the device and start using Meshtastic!

### **Option 2: Using ESP Web Flasher**
1. Go to **[ESP Web Flasher](https://esp.huhn.me/)**.
2. Click **"Connect"** and select your Heltec V2 device.
3. Ensure your **Heltec V2 is in programming mode** (see instructions above).
4. Flash each file manually to the correct address:
   - `bootloader.bin` → **0x1000**
   - `partitions.bin` → **0x8000**
   - `firmware.bin` → **0x10000**
5. Click **"Start"** and wait for the process to finish.
6. Reboot the device once flashing is complete.

## ✅ Conclusion
Your **Heltec V2** is now running **Meshtastic 2.5.22**! If you encounter any issues, ensure that the device is properly connected and in programming mode before flashing.

For more details about Meshtastic, visit the official repository: [Meshtastic on GitHub](https://github.com/meshtastic/firmware).

