
# 🔥 4-Sensor Fire Alarm System (Digital Logic Design)

This project features the design and physical implementation of an automated fire alarm system that triggers an alert only when **three or more sensors** detect a flame simultaneously. It was developed for the **Digital Logic Design (CSE345)** course at East West University.

###  Project Overview

The system uses a combination of hardware flame sensors and digital logic gates to filter out false alarms. By using a **4-to-16 line decoder**, the circuit evaluates the inputs from four different sensors and activates a buzzer/LED indicator only when a specific logic threshold (3+ sensors active) is met.

###  Key Features

* **Intelligent Triggering**: Prevents false positives by requiring a majority (3 out of 4) of sensors to be active.
* **Decoder-Based Logic**: Uses a **CD74HC154E** decoder to simplify complex Boolean expressions into hardware outputs.
* **Digital Simulation**: Includes the full digital circuit implementation designed in **Quartus II**.
* **Real-time Indicators**: Features both visual (LED) and audible (Buzzer) alerts in the physical build.

###  Repository Structure

* **`fireAlarmProject.zip`**: Contains the full Quartus II project, including the `.bdf` (Block Design File) and simulation waveforms showing the logic gate behavior.
* **`Project_report.pdf`**: Full technical documentation including the truth table, logic gates used, and photos of the physical breadboard implementation.

###  Hardware Components

* **IC 74HC154E**: 4-to-16 Line Decoder (The "brain" of the logic).
* **IC SN7404N**: Hex NOT Gates (For signal inversion from the sensors).
* **IC CD4011BE**: 4-Input OR Gate (To trigger the final alarm output).
* **LM7805**: Voltage Regulator (Steps down 9V battery to 5V).
* **Flame Sensors**: IR-based sensors for fire detection.

###  Logic Truth Table (Simplified)

The alarm activates only for the following input combinations (where 1 = Fire Detected):

| Sensor A | Sensor B | Sensor C | Sensor D | Alarm Output |
| --- | --- | --- | --- | --- |
| 1 | 1 | 1 | 0 | **ON** |
| 1 | 1 | 0 | 1 | **ON** |
| 1 | 0 | 1 | 1 | **ON** |
| 0 | 1 | 1 | 1 | **ON** |
| 1 | 1 | 1 | 1 | **ON** |
| *Other* | *Other* | *Other* | *Other* | *OFF* |

---
