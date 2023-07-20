# HC-05-Modules-in-Master-Slave-Configuration-
# How to Connect two HC-05 Modules in Master-Slave Configuration for data transmission via Bluetooth. 
Configure the HC-05 modules: Before starting the connection process, make sure both HC-05 modules are configured appropriately. You can use AT commands to set the roles and other parameters. For the master module, set it to "AT+ROLE=1" for master mode. For the slave module, set it to "AT+ROLE=0" for slave mode.

Power Supply: Connect the VCC and GND pins of both HC-05 modules to a suitable power supply. Ensure that the voltage levels match the module's requirements (usually 3.3V or 5V).

TX and RX Connections:

Connect the TX pin of the master module (HC-05 module acting as master) to the RX pin of the slave module (HC-05 module acting as slave).
Connect the RX pin of the master module to the TX pin of the slave module.
Establish a Common Ground (GND):

Connect the GND pin of the master module to the GND pin of the slave module. This establishes a common ground reference for both modules.
Optional Enable (EN) Pin:

Some HC-05 modules have an optional Enable (EN) pin. If your modules have this pin, connect the EN pin of both modules to a digital pin on your microcontroller or use a simple logic level converter to enable or disable the modules as needed.
Pairing the Modules:

Power up both HC-05 modules.
Make sure that the master module is discoverable and connectable (you can set this using AT commands if needed).
Search for available Bluetooth devices on the slave module (your phone, computer, or another Bluetooth device).
When the master module is detected, initiate the pairing process from the slave module by selecting the master module from the list of available devices.
If required, enter a PIN code during pairing (the default is usually 1234 or 0000) and confirm the connection.
Establishing a Connection:

After successful pairing, the HC-05 modules will establish a Bluetooth connection between each other.
Data can now be transmitted and received between the master and slave modules using UART communication.
Data Transmission:

Use UART communication to send and receive data between the master and slave modules.
For example, you can send control signals or sensor data from the master module to the slave module and vice versa, depending on the requirements of your Tele Operated Gesture Palm project.
Error Handling:

Implement error handling mechanisms to deal with potential issues, such as failed connections or data transmission errors, to ensure a robust and reliable communication link.
