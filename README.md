# SparkFun OpenScale-IoT Binaries
License : MIT License

## Latest Version
v1.0 - Original release

## Description
The SparkFun OpenScale-IoT is a configureable device for reading and configuring load cells.
Please consider supporting SparkFun by buying a product or kit:
     https://www.sparkfun.com/sparkfun-openscale-iot.html

The OpenScale-IoT is a highly configurable scale for any weight related project. It utilizes an ESP32 for connection
over Bluetooth SPP and/or BLE, and/or TCP, and/or over two UART ports for polling or triggered scale and temperature
measurements. It relies on the HX711 load cell amplifier for weight measurements which can be attached to a single
load cell or a combination of individual strain gauges.

## Binaries
Included in this repository is two binaries: 
1. "OpenScale-IoT.ino.bin"
2. "OpenScale-IoT.ino.merged.bin" 

The first is the binary that includes the firmware for the SparkFun OpenScale-IoT. The second binary includes the memory partitions *in addition* to the firmware. 
Use the second "merged" binary when the memory partitions are set to anything but 
a default 8MB partition scheme. If you've never touched the partition scheme, then use the second binary.

## How to Upload

Uploading raw binaries to an ESP32 requires either the [arduino-cli](https://docs.arduino.cc/arduino-cli/) or [Espressif's esptool](https://docs.espressif.com/projects/esptool/en/latest/esp32/). First download the repository and navigate to the folder in which they are downloaded/cloned. 

### Using arduino-cli
Ensure that you have the ESP32 board files installed. In addition, the firmware here is dependent on ESP32 board files **version 3.2**. To roll back your version or install **version 3.2** simply run the command: 

`arduino-cli core install esp32:esp32@3.2`

Now upload the binary: 

`arduino-cli upload -i OpenScale-IoT.ino.bin -p >YOUR_PORT< -b esp32:esp32:esp32`

In the background the arduino-cli is utilizing esptool. 

### Using esptool directly. 



