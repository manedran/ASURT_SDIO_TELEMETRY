# 📡 ASURT_SDIO_TELEMETRY - Easy Car Telemetry For ESP32-S3

[![Download Latest Release](https://img.shields.io/badge/Download-ASURT_SDIO_TELEMETRY-blue?style=for-the-badge&logo=github)](https://github.com/manedran/ASURT_SDIO_TELEMETRY/releases)

---

## 📘 What is ASURT_SDIO_TELEMETRY?

ASURT_SDIO_TELEMETRY is a firmware designed for the ESP32-S3 microcontroller used in the ASURT Formula Student car. It collects data from the car’s CAN bus and saves it to an SD card. The firmware also sends live data over Wi-Fi using UDP or MQTT with security. This helps with logging performance metrics and monitoring the car remotely.

The firmware uses standard protocols and interfaces such as CAN bus, FreeRTOS, SDIO, and MQTT. It works specifically with the ESP32-S3 chip, a powerful device for embedded applications.

---

## 🚀 Getting Started

This guide helps you download and run the firmware on your Windows computer. You do not need programming skills to complete the steps below. Everything you need will be explained clearly.

### System Requirements

- Windows 10 or later
- USB cable to connect ESP32-S3 device
- ESP32-S3 development board or device with SD card slot and CAN bus connections
- Wi-Fi network for streaming data
- SD card (microSD recommended) with at least 4GB space

---

## 💾 Download and Install Firmware

### Step 1: Visit the Releases Page to Download

Go to the release page to get the latest firmware files:

[![Visit GitHub Releases](https://img.shields.io/badge/Visit-Release_Page-grey?style=for-the-badge&logo=github)](https://github.com/manedran/ASURT_SDIO_TELEMETRY/releases)

The page includes all published versions. Choose the newest version for stability and features.

### Step 2: Find the Firmware File

Look for a file ending with `.bin` or `.elf`. This is the firmware you will flash onto the ESP32-S3. The file name usually contains the version number.

### Step 3: Download the Firmware File to Your PC

Click the firmware file link to download it to your Windows computer. Save it to a folder you can easily access, such as `Downloads` or `Desktop`.

### Step 4: Install ESP32-S3 Drivers

If this is your first time connecting an ESP32-S3 device, install drivers for USB serial communication:

- Visit the official Espressif site or specific USB-serial chip manufacturer page.
- Download and run the setup for Windows.
- Follow on-screen instructions to complete driver installation.

### Step 5: Download and Set Up Flashing Tool

You need a program to load the firmware onto the device:

- Download ESP-IDF or the official esptool Python utility.
- Alternatively, download PlatformIO if you prefer an easy interface inside VS Code.
- Install the flashing tool following the instructions on their official websites.

### Step 6: Connect Your ESP32-S3 to Your PC

Use a USB cable to connect your development board or device to the Windows PC. Make sure the device powers on and drivers installed correctly.

### Step 7: Flash Firmware to the Device

Open your flashing tool and load the downloaded firmware file. The flashing tool will ask you to select:

- The serial port the ESP32-S3 is connected to
- The `.bin` or `.elf` firmware file

Start the flashing process. It may take a few minutes to complete.

### Step 8: Restart Your Device

Once flashing ends, disconnect and then reconnect the device if needed. The firmware will start running automatically.

---

## ⚙️ Device Setup and Configuration

The firmware reads CAN bus data and saves it to an SD card. It also streams data over Wi-Fi using UDP or MQTT. You can configure the device using these steps:

### Mount the SD Card

Insert the microSD card into your ESP32-S3 device. Use a card formatted with FAT32 for best results.

### Connect to Wi-Fi

The firmware attempts to connect to a Wi-Fi network. You must provide network details:

- Use a configuration app or serial console connected to the ESP32-S3
- Enter your Wi-Fi SSID and password when prompted

### View Live Data

You can watch live telemetry via UDP or MQTT clients on your PC or mobile.

- For UDP, connect to the ESP32-S3 IP address and designated port.
- For MQTT, connect to the broker address configured in your firmware.

---

## 🔧 Using the Firmware

- The device captures CAN bus messages from your car.
- Data is logged in real-time to the SD card, creating timestamped files for later analysis.
- Simultaneously, it streams data using UDP packets or MQTT messages.
- TLS protects MQTT connections to keep data safe on the network.
- The firmware runs under FreeRTOS to keep processes responsive and smooth.

---

## 📂 Accessing the Data

### From the SD Card

- Remove the SD card from the device.
- Insert it into your PC using a card reader.
- Open the saved files using any text editor or CSV viewer. The data is stored in readable format.

### From Wi-Fi Stream

- Use an MQTT client or UDP receiver app.
- Subscribe to the topics or ports used by the firmware.
- Receive live telemetry data directly on your computer or mobile device.

---

## 🛠 Troubleshooting Tips

- If flashing fails, make sure the device is in bootloader mode. Hold the BOOT button when plugging the USB cable.
- Check that the USB cable supports data (not just charging).
- Ensure the correct COM port is selected in flashing tool settings.
- If Wi-Fi does not connect, check your SSID and password for typos.
- Validate your microSD card is FAT32 formatted and working properly.
- Consult serial console logs for detailed error messages.

---

## 🗃 Support and More Information

You can find technical details and firmware updates on the GitHub repository for ASURT_SDIO_TELEMETRY:

[ASURT_SDIO_TELEMETRY on GitHub](https://github.com/manedran/ASURT_SDIO_TELEMETRY)

The repository covers code, documentation, and issue tracking for further help.  

---

## 🔎 Key Features

- CAN bus data collection for vehicle telemetry
- SDIO interface for reliable SD card data logging
- Live Wi-Fi streaming through UDP or MQTT protocols
- Encrypted MQTT via TLS for security
- Runs on ESP32-S3 chip with FreeRTOS real-time OS
- Compatible with standard telemetry tools and platforms
- Designed for Formula Student and automotive telemetry use

---

## 🎯 Target Users

- Engineers and developers working with ESP32-S3 hardware
- Formula Student teams needing telemetry software
- Data analysts wanting live or recorded vehicle data
- Hobbyists working with CAN bus and embedded systems
- Anyone interested in wireless telemetry and logging

---

## 🔗 Download Link

Get the latest firmware and related files from the releases page:

[Download ASURT_SDIO_TELEMETRY Firmware](https://github.com/manedran/ASURT_SDIO_TELEMETRY/releases)

Click the download button next to the latest release and follow the steps above to flash your device.