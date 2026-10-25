# Vibrometer-II

Vibrometer-II is an advanced, high-performance upgrade to my original vibration monitor project. 

## The Evolution: Upgrading to RP2040

The previous version relied on an **ATmega328-P** architecture powered by twin CR2032 cells. While functional, it suffered from a bulky form factor, increased mass, and inherent measurement inaccuracies. 

To overcome these constraints, **Vibrometer-II** implements a much cleaner and faster **Raspberry Pi RP2040** core. This hardware migration achieves:
* **Drastic Form Factor Reduction:** Minimizes overall mass and physical device footprint.
* **Enhanced Measurement Accuracy:** Delivers faster data capture and processing speeds.
* **Custom Enclosure:** A brand-new structural enclosure tailored explicitly for the onboard sensor.
* **Dual-Tier UI Ecosystem:** Features advanced and basic user interfaces engineered for both high-level control and low-level system implementation.

## Technical Specifications: 

The **Vibrometer-II** uses the *LSM6DS3* as its main IMU, and the *RP2040* as the MCU. For memory, two *MX25L3233FM1* each featuring 4MB or storage.

### Individual Specifications:

#### LSM6DS3:
* Manufactured by STMicrocontrollers
* Sensor Type: 3-axis accelerometer and 3-axis gyroscope combo (6-axis IMU)
* Accelerometer Full-Scale Range: ±2 / ±4 / ±8 / ±16 g
* Gyroscope Full-Scale Range: ±125 / ±245 / ±500 / ±1000 / ±2000 dps (degrees per second)
* Power Consumption:
	• 0.9 mA in combo normal mode
	• 1.25 mA in high-performance mode (up to 1.6 kHz ODR)
	• 6 μA in power-down mode
* Supply Voltage:
	• Analog supply: 1.71V to 3.6V
	• IO supply: 1.62V
* Interface Options: SPI and I²C serial interfaces with a main processor data synchronization feature

#### RP2040:

* Manufactured by Raspberry Pi Ltd
* Core Architecture: Dual-core ARM Cortex-M0+
* Clock Frequency: Variable, running up to 133 MHz
* Internal Memory: 264 KB of on-chip SRAM divided into 6 independent banks
* External Flash Support: QSPI interface supporting up to 16 MB of external flash memory with Execute-in-Place (XIP) capabilities
* Peripherals & I/O:
	• 30 multi-function GPIO pins (26 exposed on the Pico standard form factor)
	• 2 × UART, 2 × SPI, and 2 × I2C controllers
	• 16 × PWM channels
	• 4-channel 12-bit SAR Analog-to-Digital Converter (ADC) with an integrated internal temperature sensor
* Unique Feature: 8 × Programmable I/O (PIO) state machines used to create customized hardware peripheral interfaces
* USB Interface: USB 1.1 controller supporting both Host and Device operations
* Package Options: 56-pin QFN package measuring 7×7 mm

#### MXL25L3233FM1:

* Manufacturer: Macronix International Co., Ltd.
* Memory Type: Serial Multi-I/O (MXSMIO®) CMOS NOR Flash
* Density / Capacity: 32 Megabits (Mbit), which translates to 4 Megabytes (MB)
* Interface Protocol: Serial Peripheral Interface (SPI) supporting Mode 0 and Mode 3
* I/O Width Configurations: Standard SPI (x1 I/O), Dual SPI (x2 I/O), and Quad SPI (x4 I/O) configurations
* Maximum Clock Frequency: 133 MHz
* Operating Voltage Range: 2.65V to 3.6V
* Memory Architecture:
	• 1,024 equal sectors (4 KB each)
	• 128 equal blocks (32 KB each)
	• 64 equal blocks (64 KB each)
* Standout Performance: Supports Performance Enhance Mode / Execute-in-Place (XIP) to read data without command overhead
* Operating Temperature: Industrial grade protection rating from -40°C to +85°C
* Package Form Factor: 8-pin SOP (Small Outline Package) / 8-SOIC

