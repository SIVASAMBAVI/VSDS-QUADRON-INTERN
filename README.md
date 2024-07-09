# VSDS QUARDRON MINI INTERNSHIP

*  Overview of VSDSquadron Mini Kit
*  TASK 1 - Installing the required programmes for this internship, such as Ubuntu on VMBox, Visual C++, and writing an example of C code along with evaluating RISC assembly code for the sample C code, are the tasks at hand.
*  TASK 2 - Write a simple C program for your project selected and compile with RISC-V GCC.
*  TASK 3 - To compile the C code under RISCV and equalize the output of GCC and RISCV (O1==O2).
*  TASK 4 - Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for below RISC-V instructions.
*  TASK 5 - Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment. Upload waveform snapshots for the commands on your GitHub. Reference GitHub repo is here.
  
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


*******************************************************************************************************************************************************************

## TASK 3

####  _To compile the C code under RISCV and equalize the output of GCC and RISCV (O1==O2)_

Compiling the C code both in GCC and in RISCV proves that the code can work on Kit and on chip.
With the use of an AI tool that generates the clock divided output, the C code for the project clock divider is retrieved efficiently, ensuring accurate implementation, reducing development time, and minimizing human errors, which enhances the overall reliability and performance of the clock divider.

1. C code Compilation under GCC (i.e) O1 is given below:-


![gcc output O1](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/1bbf5bf5-62fe-46ac-bb09-4fcdf905e48a)



2.  C code Compilation under RISCV (i.e) O2 is given below:-
   

![riscv output O2](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/8e10a5f4-68c8-4010-9651-14c1297f61ef)



3. Instruction codes:-

![assembly](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/89f02d27-acbe-4842-9e4b-0d19d6d1628e)



4. Assembly codes:-

![ass1](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/efc394d0-5a68-40c5-9cdd-c6603d0af537)


********************************************************************************************************************************************************************************

## TASK 4


_"Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for below RISC-V instructions_

ADD r6, r2, r1

SUB r7, r1, r2

AND r8, r1, r3

OR r9, r2, r5

XOR r10, r1, r4

SLT r11, r2, r4

ADDI r12, r4, 5

SW r3, r1, 2

SRL r16, r14, r2

BNE r0, r1, 20

BEQ r0, r0, 15

LW r13, r1, 2

SLL r15, r1, r2

_Upload the 32-bit pattern on Github"_


 #### 1 . R-Type (Register) Instructions

#### Format: Uses three registers for the operation: two source registers and one destination register.

#### Fields:

             opcode: Specifies the type of operation.
             rd: Destination register.
             funct3: Function code for additional operation specification.
             rs1: First source register.
             rs2: Second source register.
             funct7: Extended function code for further operation specification.

#### Common Instructions:

            add rd, rs1, rs2 - Integer addition.
            sub rd, rs1, rs2 - Integer subtraction.
            and rd, rs1, rs2 - Bitwise AND.
            or rd, rs1, rs2 - Bitwise OR.
            sll rd, rs1, rs2 - Shift left logical.
            sra rd, rs1, rs2 - Shift right arithmetic.


#### 2. I-Type (Immediate) Instructions

#### Format: Uses a source register and an immediate value.

#### Fields:

            opcode: Specifies the type of operation.
            rd: Destination register.
            funct3: Function code for additional operation specification.
            rs1: Source register.
            imm[11:0]: 12-bit immediate value.
            
#### Common Instructions:

            addi rd, rs1, imm - Integer addition with immediate.
            andi rd, rs1, imm - Bitwise AND with immediate.
            ori rd, rs1, imm - Bitwise OR with immediate.
            lw rd, offset(rs1) - Load word from memory.


#### 3. S-Type (Store) Instructions

#### Format: Uses two source registers and an immediate value to store data.

#### Fields:

            opcode: Specifies the type of store operation.
            imm[11:5]: High 7 bits of immediate.
            funct3: Function code for additional operation specification.
            rs1: Base address register.
            rs2: Source register containing the data to store.
            imm[4:0]: Low 5 bits of immediate.
            
#### Common Instructions:

            sw rs2, offset(rs1) - Store word to memory.
            sb rs2, offset(rs1) - Store byte to memory.


#### 4. B-Type (Branch) Instructions

#### Format: Uses two source registers and an immediate value for conditional branching.

#### Fields:

            opcode: Specifies the type of branch operation.
            imm[12|10:5]: High bits of immediate.
            funct3: Function code for branch type.
            rs1: First source register.
            rs2: Second source register.
            imm[4:1|11]: Low bits of immediate.
            
#### Common Instructions:

            beq rs1, rs2, offset - Branch if equal.
            bne rs1, rs2, offset - Branch if not equal.
            blt rs1, rs2, offset - Branch if less than.
            bge rs1, rs2, offset - Branch if greater or equal.


#### 5. U-Type (Upper Immediate) Instructions

#### Format: Used for instructions that operate with a 20-bit immediate.

#### Fields:

            opcode: Specifies the type of operation.
            rd: Destination register.
            imm[31:12]: 20-bit immediate value.
            
#### Common Instructions:

            lui rd, imm - Load upper immediate.
            auipc rd, imm - Add upper immediate to PC.

#### 6. J-Type (Jump) Instructions

#### Format: Used for jump instructions with a 20-bit immediate value.

#### Fields:

            opcode: Specifies the type of operation.
            rd: Destination register.
            imm[20|10:1|11|19:12]: 20-bit immediate value split into various segments.
            
#### Common Instructions:

            jal rd, imm - Jump and link.
            jalr rd, rs1, imm - Jump and link register (I-type format).


#### Overview of RISC-V Instruction Types

R-Type (Register): Used for arithmetic and logical operations.

I-Type (Immediate): Used for arithmetic operations with immediate values, loads, and some control instructions.

S-Type (Store): Used for storing data from registers to memory.

B-Type (Branch): Used for conditional branches.

U-Type (Upper immediate): Used for constructing large constants.

J-Type (Jump): Used for jump instructions with immediate addresses.


![ins](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/ad2b61d3-c2a6-4d53-b983-84d441f867a3)


Each instruction format has a specific structure defined by bit fields, which include the opcode, function fields, register addresses, and immediate values.

Here’s a detailed explanation of the RISC-V instructions along with their corresponding 32-bit machine codes for the specified instructions, including their exact encoding in their respective formats (R, I, S, B, U, J).


## RISC-V Instruction Formats and 32-bit Machine Codes

#### 1. *ADD r6, r2, r1*

- *Instruction*: ADD

- *Type*: R-Type

- *Format*: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | rs2[24:20] | funct7[31:25]

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r6 (0b00110)
              - funct3 = 000
              - rs1 = r2 (0b00010)
              - rs2 = r1 (0b00001)
              - funct7 = 0000000
    
#### - *32-bit Code*: 0000000 00001 00010 000 00110 0110011
 
- *Hex*: 0x0020A033

#### 2. *SUB r7, r1, r2*

- *Instruction*: SUB

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r7 (0b00111)
              - funct3 = 000
              - rs1 = r1 (0b00001)
              - rs2 = r2 (0b00010)
              - funct7 = 0100000

#### - *32-bit Code*: 0100000 00010 00001 000 00111 0110011

- *Hex*: 0x40208033

#### 3. *AND r8, r1, r3*

- *Instruction*: AND

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r8 (0b01000)
              - funct3 = 111
              - rs1 = r1 (0b00001)
              - rs2 = r3 (0b00011)
              - funct7 = 0000000

#### - *32-bit Code*: 0000000 00011 00001 111 01000 0110011

- *Hex*: 0x0030C033

#### 4. *OR r9, r2, r5*

- *Instruction*: OR

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r9 (0b01001)
              - funct3 = 110
              - rs1 = r2 (0b00010)
              - rs2 = r5 (0b00101)
              - funct7 = 0000000

#### - *32-bit Code*: 0000000 00101 00010 110 01001 0110011

- *Hex*: 0x0052C033

#### 5. *XOR r10, r1, r4*

- *Instruction*: XOR

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r10 (0b01010)
              - funct3 = 100
              - rs1 = r1 (0b00001)
              - rs2 = r4 (0b00100)
              - funct7 = 0000000

#### - *32-bit Code*: 0000000 00100 00001 100 01010 0110011

- *Hex*: 0x0040A033

#### 6. *SLT r11, r2, r4*

- *Instruction*: SLT (Set Less Than)

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r11 (0b01011)
              - funct3 = 010
              - rs1 = r2 (0b00010)
              - rs2 = r4 (0b00100)
              - funct7 = 0000000

#### - *32-bit Code*: 0000000 00100 00010 010 01011 0110011

- *Hex*: 0x00415033

#### 7. *ADDI r12, r4, 5*

- *Instruction*: ADDI (Add Immediate)

- *Type*: I-Type

- *Format*: opcode[6:0] | rd[11:7] | funct3[14:12] | rs1[19:15] | imm[31:20]

- *Encoding*:

              - opcode = 0010011 (0x13)
              - rd = r12 (0b01100)
              - funct3 = 000
              - rs1 = r4 (0b00100)
              - imm = 5 (0b000000000101)

#### - *32-bit Code*: 000000000101 00100 000 01100 0010011

- *Hex*: 0x00520113

#### 8. *SW r3, r1, 2*

- *Instruction*: SW (Store Word)

- *Type*: S-Type

- *Format*: opcode[6:0] | imm[11:7] | rs2[24:20] | rs1[19:15] | funct3[14:12] | imm[4:0]

- *Encoding*:

              - opcode = 0100011 (0x23)
              - imm[11:5] = 0 (upper part of 2 is 0)
              - rs2 = r3 (0b00011)
              - rs1 = r1 (0b00001)
              - funct3 = 010
              - imm[4:0] = 2 (0b00010)

#### - *32-bit Code*: 0000000 00011 00001 010 00010 0100011

- *Hex*: 0x00312223

#### 9. *SRL r16, r14, r2*

- *Instruction*: SRL (Shift Right Logical)

- *Type*: R-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 0110011 (0x33)
              - rd = r16 (0b10000)
              - funct3 = 101
              - rs1 = r14 (0b01110)
              - rs2 = r2 (0b00010)
              - funct7 = 0000000

#### - *32-bit Code*: 0000000 00010 01110 101 10000 0110011

- *Hex*: 0x00273333

#### 10. *BNE r0, r1, 20*

- *Instruction*: BNE (Branch Not Equal)

- *Type*: B-Type

- *Format*: opcode[6:0] | imm[11] | imm[4:1] | funct3[14:12] | rs1[19:15] | rs2[24:20] | imm[10:5] | imm[12]

- *Encoding*:

              - opcode = 1100011 (0x63)
              - imm = 20 (0b0000000001010)
              - rs1 = r0 (0b00000)
              - rs2 = r1 (0b00001)
              - funct3 = 001

#### - *32-bit Code*: 0000000 00101 00001 001 00000 1100011

- *Hex*: 0x01408063

#### 11. *BEQ r0, r0, 15*

- *Instruction*: BEQ (Branch Equal)

- *Type*: B-Type

- *Format*: Same as above.

- *Encoding*:

              - opcode = 1100011 (0x63)
              - imm = 15 (0b0000000000111)
              - rs1 = r0 (0b00000)
              - rs2 = r0 (0b00000)
              - funct3 = 000

#### - *32-bit Code*: `0000000 000


************************************************************************************************************************************************************************************************************

## TASK 5

_Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment. Upload waveform snapshots for the commands on your GitHub. Reference GitHub repo is here._


 ### ✒️Note With reference to these github repo's  and using AI tool the below has been developed :- https://github.com/maazm007/vsdsquadron-mini-internship  // https://github.com/vinayrayapati/rv32i/

 ## Overview

1. Clone the Reference Repository

2. Set Up Simulation Tools (GTKWave)

3.  Edit the Testbench File:

4. Run the Functional Simulation


## Process:-


#### 1. Clone the Reference Repository

First, clone the repository that contains the Verilog netlist and testbench:

          $ git clone https://github.com/vinayrayapati/rv32i.git my_riscv_project
          
          $ cd my_riscv_project

  You can provide your name in the place of my_riscv_project!!

![clone](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/f39b7d74-04a0-44fe-8b01-b314c8deadcb)


#### 2. Set Up Simulation Tools (iverilog and GTKWave)

Install Icarus Verilog and GTKWave for Verilog simulation and waveform viewing.


          $ sudo apt update
          
          $ sudo apt install iverilog gtkwave

![update](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/ce67583d-9fba-4f76-a346-729cd7495750)

![install](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/90fffb63-cd38-49cf-8aa6-1abe9692eacf)


#### 3. Edit the Testbench File:

Open the testbench file in a text editor:

          $ nano iiitb_rv32i_tb.v

After providing the above command press "ctrl+x" to release and check for that your testbench is in same format provided below:-

#### EXAMPLE:-
  
    initial begin
    
      $dumpfile("simulation.vcd"); // Name of the VCD file
   
      $dumpvars(0, testbench); // Dump all signals of the testbench module
 
      end
  
      // Testbench code...

    endmodule

  ![nanoedit](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/6ca510af-3aa1-49e0-9be7-3a2d0d5c0e00)
  

Ensure your testbench is configured to dump waveforms into a _.vcd file._ Here's a basic example of how your testbench might be configured:


#### 4. Run the Functional Simulation
  
_Signals and instantiation of the design_

Compile and Simulate:

        $ iverilog -o rv32i_simulation iiitb_rv32i.v iiitb_rv32i_tb.v
        
        $ vvp rv32i_simulation


![vvp command](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/e3839e3f-fced-400f-8438-25be9e5d2163)

View the Waveform:

        $ gtkwave simulation.vcd


* After giving the above command  gtkwave window will open .
  
* Then,click the "+" icon near iiitb_rv32_tb  so that rv32 will pop out.
  
* Nextly, at the bottom choose the  command from signals below for displaying waveform. once after you chose a command do not forget to give append at the bottom left corner of you screen.
  
* And now, the waves will be vsible on your blck screen as shown in the picture below.


 ## OUTPUT:-

 #### ADD:-

 ![add](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/0b436ed7-3766-4d7c-9362-5eb30a715c7d)

 #### ADDI:-
 
![addi](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/030d07b7-1e3b-46dd-be49-b25e0378ec47)


#### SUB:-

![sub](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/8fd47b54-3aa9-483b-802e-c2c53d38b01a)

#### AND:-

![and](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/5e92113f-d3f0-482b-990f-9839e42c226e)

#### OR:-

![or](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/3187f744-616a-4ab2-844d-ad05aa5e402d)

#### XOR:-

![xor](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/944d1ece-637b-492f-bc60-af839f1b4b7d)

#### SLT:-

![slt](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/c219a2b4-4fad-457f-b27b-fa20f45a534b)

#### BEQ:-

![beq](https://github.com/SIVASAMBAVI/VSDS-QUADRON-INTERN/assets/150532409/55be53ff-05e1-42c2-8d9b-1b26d6122303)

*************************************************************************************************************************************************************************************************************************************
## TASK 6:-

Here's the updated documentation for "Clock Cycle Divider: Crafting a Digital Clock Divider Circuit" using a RISC-V processor without an FPGA board or external clock:

### Project Name

_Clock Cycle Divider: Crafting a Digital Clock Divider Circuit Using RISC-V Processor._

### Overview
This project involves designing a digital clock divider circuit using a RISC-V processor, without relying on an FPGA board or external clock. Instead, the RISC-V processor generates the clock signal internally and divides it through software. This approach allows flexibility in creating different clock frequencies for various subsystems by programming the division factor.

### Components Required
- RISC-V Processor Development Board: To generate and divide the clock signal.
- Internal Clock Generator: Built-in clock of the RISC-V processor.
- General Purpose Input/Output (GPIO) Pins**: Used for interfacing the divided clock signal.
- Power Supply: For the RISC-V development board.
- Jumper Wires: For connections.
- Breadboard: Optional, for prototyping connections.
- Oscilloscope/Logic Analyzer: For testing and verification.

### Circuit Connection

1. RISC-V Processor Development Board:
    - Use the internal clock of the RISC-V processor to generate the clock signal.
    - Configure GPIO pins for the output of the divided clock signal.
2. Output:
    - The divided clock signal is output through a GPIO pin.
    - Connect the output pin to an oscilloscope or logic analyzer for verification.

#### Implementation Steps:

1. RISC-V Software: Develop the software to generate the initial clock signal and perform clock division based on a user-defined factor.
2. Clock Handling: Use a software timer or a loop to generate the initial clock signal and implement the division logic.
3. Signal Output: Output the divided clock signal through a GPIO pin, toggling the state based on the divided clock period.
4. Testing: Test the divided clock output using an oscilloscope or logic analyzer to verify the frequency and stability.


#### Pinout Diagram



### Table for Pin Connection

| Component              | Pin Name/Number | Connection Description                              |
|------------------------|------------------|-----------------------------------------------------|
| RISC-V Processor       | GPIO Clock Input | Internally generated clock signal                   |
| RISC-V Processor       | GPIO Output Pin  | Outputs the divided clock signal                    |
| Power Supply           | VCC, GND         | Powers the RISC-V development board                 |

### Example Pin Connections:

- RISC-V Internal Clock → Handled by RISC-V Software
- **RISC-V GPIO Output Pin → Test Point/Output Connector

### Software Example

Below is a basic example of how you might implement the clock divider in C for a RISC-V processor:

```c
#include <stdint.h>
#include <gpio.h>
#include <timer.h>

// GPIO configuration for the RISC-V platform
#define CLOCK_OUTPUT_PIN 1 // GPIO pin for clock output

// Division factor
volatile uint32_t div_factor = 4; // Set to divide by 4 for example

void delay(uint32_t cycles) {
    for (volatile uint32_t i = 0; i < cycles; i++);
}

void generate_clock(uint32_t frequency) {
    uint32_t period = 500000 / frequency; // Calculate period for desired frequency

    while (1) {
        gpio_write(CLOCK_OUTPUT_PIN, 1); // Set output high
        delay(period / div_factor);      // Delay for half period
        gpio_write(CLOCK_OUTPUT_PIN, 0); // Set output low
        delay(period / div_factor);      // Delay for half period
    }
}

int main() {
    gpio_config(CLOCK_OUTPUT_PIN, GPIO_OUTPUT);

    // Set desired frequency
    uint32_t frequency = 1; // Example: 1 Hz initial clock

    generate_clock(frequency);
    return 0;
}
```

### Detailed Steps:

1. Configure GPIO: Initialize GPIO pins for clock output.
2. Generate Initial Clock: Implement a function to generate the initial clock signal using a timer or loop.
3. Implement Division Logic: Divide the clock by toggling the GPIO output based on the division factor.
4. Control Logic: Implement control logic to adjust the division factor dynamically via control pins or software commands if needed.

### Testing and Verification:

1. Run the RISC-V Program: Upload and execute the clock divider program on the RISC-V development board.
2. Measure Output: Use an oscilloscope to measure the frequency of the output clock signal and verify that it matches the expected divided frequency.


#### ✒️NOTE:- The above provides a comprehensive overview of the clock cycle divider project using a RISC-V processor without external clock sources or FPGA boards. Ensure to adjust the software logic based on the specific RISC-V platform and your application's requirements.
 
 





















           
           
