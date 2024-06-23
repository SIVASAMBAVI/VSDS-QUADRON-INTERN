VSDS QUADRON MINI INTERNSHIP
           
A detailed description of the kit is given below.
            
            
![risc-v](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/9ea472b3-b49a-42be-bad2-fc65c15ca07d)

### Overview of VSDSquadron Mini Kit

The **VSDSquadron Mini** is a compact development board featuring a **RISC-V microcontroller**, ideal for educational and experimental use.

### Features:

- **RISC-V Core:** Open-source ISA-based CPU for flexibility and innovation.
- **USB Connectivity:** USB Type-C for power and data.
- **GPIO Headers:** For connecting peripherals.
- **Debugging Interface:** SWD interface for debugging.
- **On-Board Buttons:** Includes reset and user-programmable buttons.
- **Voltage Regulation:** Ensures stable power supply.

### Components:

- **USB Type-C Connector:** For power and data communication.
- **Microcontroller:** RISC-V core.
- **Voltage Regulators:** For stable power.
- **Pin Headers:** Expose I/O pins.
- **SWD Interface:** For programming/debugging.
- **Buttons:** Reset and user buttons.

### Pin Diagram:

- **Power Pins:** 5V, 3.3V, GND.
- **Communication Pins:** RX (UART input), TX (UART output).
- **Debugging Pins:** SWDIO, SWCLK.
- **GPIO Pins:** PC0-PC7, PD0-PD7.
- **Other Pins:** RST (reset), BOOT (bootloader mode).

### Applications:

- **Learning & Experimentation:** For RISC-V programming and hardware interfacing.
- **Prototyping:** For embedded systems and IoT devices.
- **Peripheral Interface:** Connects with sensors and actuators.
- **Firmware Development:** Supports firmware development with SWD debugging.

### Programming:

- **Toolchains:** Uses GCC for RISC-V.
- **IDE Support:** Compatible with RISC-V IDEs.
- **Code Upload:** Via USB using tools like OpenOCD.

This board is a versatile tool for exploring RISC-V architecture and developing embedded applications.


Installing the required programmes for this internship, such as Ubuntu on VMBox, Visual C++, and writing an example of C code along with evaluating RISC assembly code for the sample C code, are the tasks at hand.

Step 1. Setting up Ubuntu within VMBox
Once the tools have been installed, launch Ubuntu's terminal and enter the command.

Step 2. Order for Leafpad Installation
            $ sudo apt install leafpad
        
Step 3. To open Leafpad
            $ cd 
            $ leafpad filename.c &
![PROGRAM](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/7cdc08c8-5e9f-4b92-a68d-8a3651c9ca35) ------------>PROGRAM

Step 4. Order for Gathering and Examining the Results
            $ gcc filename.c
            $./a.out
![OUTPUT](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/3e8c9962-a4c8-44a9-a396-a4f84235fe9d)  --------------->OUTPUT

Step 5. Command for RISC-V Compiler Code Compilation
        $ riscv64-unknown-elf-gcc-O1 -mabi=lp64 -march=rv64i -o filename.o filename.c 
        $ ls filename.o -ltr
![1](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/948a3682-e196-4ba5-9e72-dc4593979ccd) ----------------->ASSEMBLY CODE 1

Step 6. Press to Display the Assembly Code
        $ riscv64-unknown-elf-objdump-d filename.o ------>Provides a large amount of code
        $ riscv64-unknown-elf-objdump -d filename.o | less ------->Provides Reduced Code /main and to see the code's primary function
![2](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/1c574c97-64af-477e-8a06-e944a45afca0) ---------------->ASSEMBLY CODE 2

Step 7. Order to Examine Assembly Code
         $ riscv64-unknown-elf-gcc-Ofast -mabi=lp64 -march=rv64i -o filename.o filename.c 
         $ riscv64-unknown-elf-objdump -d filename.o | less /main 





           
           
