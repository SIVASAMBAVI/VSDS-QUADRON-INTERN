# VSDS QUARDRON MINI INTERNSHIP

*  Overview of VSDSquadron Mini Kit
*  TASK 1
*  TASK 2
****************************

_A detailed description of the kit is given below._
            
            
![risc-v](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/9ea472b3-b49a-42be-bad2-fc65c15ca07d)

### Overview of VSDSquadron Mini Kit
*************************************

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

*********************************************************************************************************************************************************************************************************************


## TASK 1

#### _Installing the required programmes for this internship, such as Ubuntu on VMBox, Visual C++, and writing an example of C code along with evaluating RISC assembly code for the sample C code, are the tasks at hand._

#### Step 1. Setting up Ubuntu within VMBox
Once the tools have been installed, launch Ubuntu's terminal and enter the command.

#### Step 2. Order for Leafpad Installation

        $ sudo apt install leafpad
        
#### Step 3. To open Leafpad

        $ cd 
        
        $ leafpad filename.c &
        
        
![program1](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/d121f5f5-7c83-4b94-b68b-dc117915ab46)



#### Step 4. Order for Gathering and Examining the Results

        $ gcc filename.c
        
        $./a.out

        
![output](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/40210207-6361-4a40-99b6-48b68800da13)



#### Step 5. Command for RISC-V Compiler Code Compilation

        $ riscv64-unknown-elf-gcc-O1 -mabi=lp64 -march=rv64i -o filename.o filename.c 
        
        $ ls filename.o -ltr



#### Step 6. Press to Display the Assembly Code

        $ riscv64-unknown-elf-objdump-d filename.o ------>Provides a large amount of code
        
        $ riscv64-unknown-elf-objdump -d filename.o | less ------->Provides Reduced Code /main and to see the code's primary function

![ass](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/e12e50f5-8a91-4872-a445-c662c7f7e320)   



#### Step 7. Order to Examine Assembly Code

        $ riscv64-unknown-elf-gcc-Ofast -mabi=lp64 -march=rv64i -o filename.o filename.c 
        
        $ riscv64-unknown-elf-objdump -d filename.o | less /main 

![main](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/1116f104-0879-468d-920c-7b66cd35af8a)

*********************************************************************************************************************************************************************************************************************

## TASK 2

#### _Write a simple C program for your project selected and compile with RISC-V GCC_

A clock divider is a circuit that divides the frequency of a clock signal. It's used in digital systems to create slower clocks from a high-speed clock source. For example, a clock divider can take a 100 MHz clock and produce a 50 MHz clock. Clock dividers are fundamental in digital electronics and are used in timing, synchronization, and power management.


#### CODE:-


![clock_divider program and output n=10](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/9e9028b5-a6cc-47b5-955e-5ed2aa52bc45)


The provided code simulates this process using a simple loop:

Initialization:

clock toggles to simulate the input clock.
dividedClock represents the output clock signal.
counter counts the input clock cycles.
Clock Simulation:

The clock variable toggles between 0 and 1 to simulate the input clock signal.
Clock Division:

On each positive edge of the clock (clock == 1), the counter increments.
When the counter equals the specified value 
𝑛
n, the dividedClock toggles, and the counter resets to 0.

*******************************************************************

#### Timing Diagram


![TIMING DIAGRAM](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/000cb2fa-70d9-4d8c-b1b3-8c3ebdb8054b)


Here is a basic timing diagram illustrating the input clock and the divided clock output for a clock divider with 𝑁=10.


**************************************************************************************************************************************


#### BLOCK DIAGRAM:-


![Simple Basic Flowchart Diagram](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/d4afc750-d521-47d0-b7ae-0cc936849e24)

************************************************************************************************************************************************************

#### ASSEMBLY CODES:

![assembly1](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/aa0be868-b957-4860-97a3-2bd27f99b4c6)


![assembly2](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/9cbe7e50-e651-4472-8253-26bb74a60331)


![assembly3](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/92f2296a-e7ce-48f9-94ce-853f8aad0bc7)


![assembly4](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/9b9c6e5e-cf25-4cbb-b014-199600443f66)


*******************************************************************************************************************************************************************8

## TASK 3

####  _To compile the C code under RISCV and equalize the output of GCC and RISCV (O1==O2)_

Compiling the C code both in GCC and in RISCV proves that the code can work on Kit and on chip.

C code Compilation under RISCV is given below:-



















           
           
