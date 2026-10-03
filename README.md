# Advanced-Footstep-Power-Generation-System

## Project Overview

The Footstep Power Generation system is a non-conventional energy generation system that converts the mechanical energy produced by human footsteps into electrical energy.
The system uses piezoelectric sensors to convert the force and pressure produced by footsteps into electrical energy. The generated electrical output is processed through a bridge rectifier and a DC-DC boost converter before being stored in a battery.
An Arduino UNO is used as the main control unit. The system also includes an RFID reader, LCD display, relay module, LEDs, voltmeter, and volt-ammeter. RFID is used to provide authorized access to the stored power, while the LCD displays the access status and allotted power usage time.
The stored energy can be utilized for applications such as mobile phone charging and other suitable electrical loads.

## Objectives

- To generate electrical power from human footsteps.
- To convert mechanical energy from footsteps into electrical energy.
- To store the generated electrical energy in a rechargeable battery.
- To use piezoelectric sensors for converting force and pressure into electrical signals.
- To provide controlled access to the stored electrical power.
- To display system and access information using an LCD.
- To utilize the stored energy for applications such as mobile charging.
  
## Working Principle

The working of the system is based on the piezoelectric effect.
When physical pressure is applied to the piezoelectric sensors through a human footstep, the sensors generate electrical energy. The generated output is then passed through a bridge rectifier to convert the AC output into pulsating DC.
The output from the rectifier is supplied to a DC-DC boost converter. The boost converter increases the voltage to the required level for the storage battery.
The generated energy is stored in the battery. A voltmeter is used to show the battery voltage, while the volt-ammeter is used to observe voltage and current.
The Arduino UNO controls the power access system. An RFID reader is used to identify an authorized RFID card. When an authorized card is detected, the Arduino activates the relay and provides power for the allotted time. The LCD displays the access status and power usage information, while green and red LEDs indicate the corresponding access status.

## System Flow

Footstep Pressure
        ↓
Piezoelectric Sensors
        ↓
Bridge Rectifier
        ↓
DC-DC Boost Converter
        ↓
Storage Battery
        ↓
Relay Controlled Output
        ↓
Mobile USB / Electrical Load

The Arduino UNO controls the RFID-based access system, LCD display, LEDs, and relay.

## Main Components

- Arduino UNO
- Piezo Sensors
- RFID Reader RC-522
- RFID Cards/Tags
- 5V DC Relay Module
- XL6009 Boost Converter
- 1 Amp Bridge Rectifier
- 12V Battery Pack using 18650 cells
- I2C LCD Driver
- 16x2 LCD Display
- Voltmeter
- Volt-Ammeter
- 5V USB Charger
- 7805 IC
- Heat Sink
- On/Off Toggle Switch
- DC Jack
- 12V Adapter
- PCB Board
- LEDs
- 220 ohm Resistors
- Wires
- Rubber Sleeves
- Male and Female Headers
  
## Piezoelectric Sensor Arrangement

The supplied project report describes connecting piezoelectric transducers using a series and parallel arrangement.
Three piezoelectric transducers were connected in series, and three such sets were connected in parallel to form a series-parallel arrangement. The output voltage and current were checked using a multimeter.
The report also describes placing a small glue stick on the top of the piezoelectric transducer to maximize its output.

## Control System

The Arduino UNO acts as the main control unit.
The project code uses:
- SPI communication for the RFID reader
- MFRC522 library for the RC-522 RFID reader
- I2C LCD for displaying information
- Relay control for power access
- Green LED for authorized access
- Red LED for denied or inactive access

## RFID-Based Power Access

The system provides controlled access to the stored power using an RFID card.
When an authorized RFID card is detected, the LCD displays:
"Authorized access"
and
"2min Power O/P"
The relay is then activated and the green LED indicates authorized access. After the allotted time, the relay is deactivated and the red LED is turned on.
If an unauthorized RFID card is detected, the LCD displays the card ID and:
"Access denied"
 supplied code uses RFID reader pins with SS on pin 10 and RST on pin 9. The relay control is defined on pin 7, while the green and red LEDs are connected to pins 5 and 6 respectively.
 
## LCD Display

The LCD is connected through an I2C module to reduce the number of connections.
The LCD is used to display:
- Footstep generator status
- Power storage status
- RFID access status
- Authorized access
- Access denied
- Power output time

## Circuit

The circuit contains the following major sections:
1. Piezoelectric energy generation
2. Bridge rectifier
3. DC-DC boost converter
4. Storage battery
5. Voltage and current measurement
6. Arduino UNO control unit
7. RFID reader
8. I2C LCD
9. Relay module
10. Controlled output

## Applications

The project material identifies applications such as:

- Railway stations
- Bus stations
- Airports
- Malls
- Footpaths
- Dancing floors
- Rural areas
- Areas with large numbers of people

The concept is particularly related to locations where large numbers of people move continuously.

## Advantages

The project provides a method of utilizing energy produced through human footsteps.

It can be used to demonstrate:

- Non-conventional energy generation
- Mechanical-to-electrical energy conversion
- Piezoelectric energy harvesting
- Battery energy storage
- RFID-based access control
- Embedded system control

## Limitations and Troubleshooting

During development, the project report describes several practical issues.

The volt-ammeter initially showed an incorrect current reading and was later replaced.

Some piezoelectric sensors were affected during soldering because excessive temperature could reduce their efficiency.

Incorrect polarity and wiring also produced negative voltage readings. The connections were checked and corrected to resolve the issue.

## Future Scope

The supplied project report proposes further development of the system using specially designed flooring tiles containing piezoelectric materials.

Such flooring can be installed in locations with large crowd movement, including railway stations, bus stations, airports, malls, and footpaths.

The report also discusses the possibility of using the technology for large-scale electricity generation and integrating the system with other power sources such as grid backup and solar energy to create a hybrid system.

## Conclusion

The Footstep Power Generation project demonstrates the conversion of human footstep energy into electrical energy using piezoelectric sensors.

The generated energy can be processed and stored in a battery and can subsequently be used for suitable electrical applications. The integration of Arduino UNO, RFID, LCD, relay, and LED indicators provides controlled access to the stored power.
