#  Samsung RISC-V Talent Development Program 2025

RISC-V Talent Development Program, Empowering future innovators, this program is powered by Samsung Semiconductor India Research (SSIR) in collaboration with VLSI System Design (VSD).
The program is led by the esteemed Kunal Ghosh, a trailblazer in the VLSI domain.

##  About Me

**Name:** ADITHYA  
**College:** Sahyadri College of Engineering and Management  
**Branch:** Electronics and Communication         
**Year:** 2nd Year         
**Email:** adithyar.ec23@sahyadri.edu.in / adithyarg14@gmail.com   

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/adithyarg?tab=repositories)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adithya-rg-74a23b293/)


----------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 1:</b> Installation of essential tools required for this internship such as Ubuntu on VMBox and refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler</summary>   
<br>

### Installed Ubuntu 18.04 LTS on Oracle Virtual Machine Box**
- Downloaded the RISC-V workshop VDI file.
- Installed Oracle VirtualBox and created a virtual machine with the following specifications:
  - **RAM:** 4 GB  
  - **CPU Cores:** 4  
  - **Operating System:** Linux-based Ubuntu 18.04 LTS
- Successfully set up the virtual environment and folder structure for further tasks.

![Ubuntu and VMBox Installation](https://github.com/adithyarg/samsung-riscv/blob/b59cedf0872e46a028c4f9a2169a92985824331f/Task%20-%201/Ubuntu%20and%20VMBox%20Installation.png)

---

### C Language based LAB
We have to follow the given steps to compile any **.c** file in our machine:
1. Open the bash terminal and locate to the directory where you want to create your file. Then run the following command:

	```
	$ cd
	$ sudo apt install leafpad
	$ leafpad sum1ton.c &
	```
 2. This will open the editor and allows you to write into the file that you have created. You have to write the C code of printing the sum of n numbers. Once you are done with your code, press ```Ctrl + S``` to save your file, and then press ```Ctrl + W``` to close the editor.   

![Developed a C program.](https://github.com/adithyarg/samsung-riscv/blob/8f1408c19e6ff497027abb9b34e66398c7efffc0/Task%20-%201/Code%20of%20C%20based%20lab.png)

3. To the C code on your terminal, run the following command:
	```
	$ gcc sum1ton.c
	$ ./a.out
	```
![Executed a C program.](https://github.com/adithyarg/samsung-riscv/blob/c69125f8dbb45277759690c3d67f8f0d9d2511cf/Task%20-%201/C%20Code%20compiled%20on%20gcc%20Compiler.png)

  
------------------------------------------------------------------------------------------------------------------

### RISCV based LAB
We have to do the same compilation of our code but this time using RISCV gcc compiler. Follow the given steps:  
1. Use the cat command to display the content of the sum1ton.c file in the terminal: 

	```
	$ cat sum1ton.c
	```
![cat Command](https://github.com/adithyarg/samsung-riscv/blob/610e60ce566fd879ff0601b4046d560e4882e05f/Task%20-%201/cat%20Command.png)

2. Using the **cat** command, the entire C code will be displayed on the terminal. Compile with Optimization Level O1
Compile the code using the RISC-V GCC compiler with the following flags:

	```
	$ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

3. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	$ riscv64-unknown-elf-objdump -d sum1ton.o | less
	```
4. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.

![Objdump using -O1 format](https://github.com/adithyarg/samsung-riscv/blob/70786f6c2ee6d9739941617fa637965772c3abd2/Task%20-%201/Objdump%20using%20-O1%20format.png)

5. Compile with Optimization Level Ofast, Compile the code using the RISC-V GCC compiler with the following flags:

	```
	$ riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

6. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	$ riscv64-unknown-elf-objdump -d sum1ton.o | less
	```
7. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.

![Objdump using -Ofast format](https://github.com/adithyarg/samsung-riscv/blob/5508c53ce209c8721039736cb7cceb97dc5a8f73/Task%20-%201/Objdump%20using%20-Ofast%20format.png)

### *Descriptions of the keyword used in above command*   
* **-O1:** Basic optimization level.
* **-Ofast:** Maximum optimizations for speed, potentially altering standard behavior.
* **-mabi=lp64:** Specifies the ABI (Application Binary Interface) for 64-bit architecture.  
* **-march=rv64i:** argets the 64-bit RISC-V base integer instruction set.
* **-o sum1ton.o:** Specifies the output file name.

Comparison of **-O1:** and **-Ofast:**
The -Ofast flag typically reduces the number of instructions by using advanced techniques like loop unrolling, vectorization, and other performance-enhancing strategies, resulting in faster code execution compared to -O1.
</details>

-------------------------------------------------

<details>
<summary><b>Task 2:</b> Running SPIKE Simulation with Compiler Optimization and Analyzing RISC-V Object Dumps</summary>   
<br>
	
### C Language based Factorial Code
We have to follow the given steps to compile any **.c** file in our machine:
1. Open the bash terminal and locate to the directory where you want to create your file. Then run the following command:

	```
	$ cd
 	$ leafpad factofnum.c &
	```
 2. This will open the editor and allows you to write into the file that you have created. You have to write the C code of printing the factorial of 5. Once you are done with your code, press ```Ctrl + S``` to save your file, and then press ```Ctrl + W``` to close the editor.  

![Developed a C program.](https://github.com/adithyarg/samsung-riscv/blob/6af07b893f4fce1ef6759ffc84705d234c831496/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/factorial_code.png)

### Factorial Code Compilation and Output 
We have to follow the given steps to get output any **.c** file in our machine:
1. To the C code on your terminal, run the following command:

	```
	$ gcc sum1ton.c
	$ ./a.out
	```
![Executed a C program.](https://github.com/adithyarg/samsung-riscv/blob/69e63628eb6d72c94bdb5a2e6abef6ef9adf782d/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/factorial_code_output.png)

### Factorial Code Spike Output
We have to follow the given steps to get output any **.c** file in our machine:
1. To the C code on your terminal, run the following command:

	```
	$ spike pk factofnum.o
	```
![Executed a C program using Spike functtion.](https://github.com/adithyarg/samsung-riscv/blob/1ec8ef880ee8793fd28ba7d75c4bbeff4ec0638d/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/factorial_output_spike.png)

### Compile with Optimization Level -O1
We have to do the same compilation of our code but this time using RISCV gcc compiler. Follow the given steps:  
1. Compile the code using the RISC-V GCC compiler with the following flags:

	```
	$ riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o factofnum.o factofnum.c
	```

2. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	$ riscv64-unknown-elf-objdump -d factofnum.o | less
	```
3. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.

![Objdump using -O1 format](https://github.com/adithyarg/samsung-riscv/blob/2466c7383f4c996598b59b16c06145790ef313db/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/main_factorial_O1.png)

### Compile with Optimization Level -Ofast
We have to do the same compilation of our code but this time using RISCV gcc compiler. Follow the given steps:  
1. Compile the code using the RISC-V GCC compiler with the following flags:

	```
	$ riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o factofnum.o factofnum.c
	```

2. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	$ riscv64-unknown-elf-objdump -d factofnum.o | less
	```
3. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.

![Objdump using -Ofast format](https://github.com/adithyarg/samsung-riscv/blob/167ec55e2b8dd5cf7629e3d4ca7073472552a600/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/main_factorial_Ofast.png)

### Debug with Optimization Level -O1	
We have to do the same compilation of our code but this time using SPIKE debug compiler. Follow the given steps:  
1. Compile the code using the SPIKE debug compiler with the following flags:

	```
	$ spike -d pk factofnum.o
	$ until pc 0 101d4
	$ reg 0 sp
	$ q
	$ spike -d pk factofnum.o
	$ until pc 0 101d4
	$ reg 0 sp

	$ reg 0 sp
	```

![Spike debug -01 format](https://github.com/adithyarg/samsung-riscv/blob/7928ee8141cf2d5b333444dca84c4e96a9d7ff8a/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/spike_debug_factorial_O1.png)

### Debug with Optimization Level -Ofast	
We have to do the same compilation of our code but this time using SPIKE debug compiler. Follow the given steps:  
1. Compile the code using the SPIKE debug compiler with the following flags:

	```
	$ spike -d pk factofnum.o
	$ until pc 0 100b0
	$ reg 0 a0

	$ reg 0 a0

	$ reg 0 sp
	$ q
	$ spike -d pk factofnum.o
	$ until pc 0 100b4

	$ reg 0 sp
	```

![Spike debug -0fast format](https://github.com/adithyarg/samsung-riscv/blob/4734bb6b77648581fc02f866ed1411349eef1465/Task%20-%202/simple%20C%20program%20(Factorial%20of%205)/spike_debug_factorial_Ofast.png)


</details>

-------------------------------------------------

<details>
<summary><b>Task 3:</b> Identify 15 unique RISC-V instructions and decode their 32-bit binary representations</summary>   
<br>

### Brief Overview of RISC-V Instruction Formats
**1. R-Type Instruction**

* Purpose: Used for arithmetic and logical operations on registers.
> * opcode (7 bits): Identifies the instruction type.
> * rd (5 bits): Destination register to store results.
> * func3 (3 bits): Specifies the operation type.
> * rs1 (5 bits): First source register.
> * rs2 (5 bits): Second source register.
> * func7 (7 bits): Further specifies the operation type.
Example: add x1, x2, x3 (Adds x2 and x3, stores in x1).

**2. I-Type Instruction**
* Purpose: Used for immediate and load operations involving registers and immediate values.
Fields:
> * opcode (7 bits): Identifies the instruction type.
> * rd (5 bits): Destination register to store results.
> * func3 (3 bits): Specifies the operation type.
> * rs1 (5 bits): Source register.
> * imm[11:0] (12 bits): Signed immediate value.
> * Example: addi x1, x2, 10 (Adds x2 and 10, stores in x1).

**3. S-Type Instruction**
* Purpose: Used for store operations, writing data from a register to memory.
> * opcode (7 bits): Identifies the instruction type.
> * imm[11:5] (7 bits): Upper bits of the signed immediate value.
> * rs1 (5 bits): Base address register.
> * rs2 (5 bits): Source register (data to store).
> * func3 (3 bits): Specifies the width/type of data (byte, half-word, word).
> * imm[4:0] (5 bits): Lower bits of the signed immediate value.
> * Example: sw x2, 8(x3) (Stores x2 at address x3 + 8).

**4. B-Type Instruction**
* Purpose: Used for conditional branching based on comparisons.
> * opcode (7 bits): Identifies the instruction type.
> * imm[12], imm[10:5], imm[4:1], imm[11]: Encodes a 12-bit signed immediate value.
> * rs1 (5 bits): First source register.
> * rs2 (5 bits): Second source register.
> * func3 (3 bits): Specifies the comparison type (e.g., equal, less than).
> * Example: beq x1, x2, label (Branches to label if x1 == x2).

**5. U-Type Instruction**
* Purpose: Used to load upper immediate values into registers.
> * opcode (7 bits): Identifies the instruction type.
> * rd (5 bits): Destination register to store results.
> * imm[31:12] (20 bits): Upper 20 bits of the immediate value.
> * Example: lui x1, 0x12345 (Loads 0x12345000 into x1).

**6. J-Type Instruction**
* Purpose: Used for unconditional jumps, including function calls.
> * opcode (7 bits): Identifies the instruction type.
> * rd (5 bits): Destination register (stores return address).
> * imm[20], imm[10:1], imm[11], imm[19:12]: Encodes a 20-bit signed immediate value (jump offset).
> * Example: jal x1, label (Jumps to label and stores return address in x1).


### Analysis of Instructions
![Objdump of application code.](https://github.com/adithyarg/samsung-riscv/blob/b1359c7c46d669c55984484888cb12549cf77649/Task%20-%203/main_factorial_Ofast.png)

1. **Instruction at address 0x1000b0:**
   ```
   ADD a0, a0, x1
   ```
   - Type: R-Type
   - Opcode: 0110011
   - `rd` = `a0` = `x10` = 01010
   - `rs1` = `a0` = `x10` = 01010
   - `rs2` = `x1` = 00001
   - `func3` = 000
   - `func7` = 0000000

   **32-bit representation:**
   ```
   0000000_00001_01010_000_01010_0110011
   ```

2. **Instruction at address 0x1000b4:**
   ```
   ADDI sp, sp, -16
   ```
   - Type: I-Type
   - Opcode: 0010011
   - `rd` = `sp` = `x2` = 00010
   - `rs1` = `sp` = `x2` = 00010
   - Immediate = -16 = `1111111111110000` (12-bit, signed)

   **32-bit representation:**
   ```
   111111111111_00010_000_00010_0010011
   ```

3. **Instruction at address 0x1000b8:**
   ```
   LI a1, 5
   ```
   - Pseudoinstruction for `ADDI a1, x0, 5`
   - Type: I-Type
   - Opcode: 0010011
   - `rd` = `a1` = `x11` = 01011
   - `rs1` = `x0` = 00000
   - Immediate = 5 = `000000000101`

   **32-bit representation:**
   ```
   000000000101_00000_000_01011_0010011
   ```

4. **Instruction at address 0x1000bc:**
   ```
   LUI a0, 464
   ```
   - Type: U-Type
   - Opcode: 0110111
   - `rd` = `a0` = `x10` = 01010
   - Immediate = 464 << 12 = `000000000000011101000000000000`

   **32-bit representation:**
   ```
   00000000000001110100_01010_0110111
   ```

5. **Instruction at address 0x1000c0:**
   ```
   JAL ra, 8
   ```
   - Type: J-Type
   - Opcode: 1101111
   - `rd` = `ra` = `x1` = 00001
   - Offset = 8 (signed 20-bit)

   **32-bit representation:**
   ```
   00000000000000000000_00001_1101111
   ```

6. **Instruction at address 0x1000c4:**
   ```
   ADDI sp, sp, 16
   ```
   - Type: I-Type
   - Opcode: 0010011
   - `rd` = `sp` = `x2` = 00010
   - `rs1` = `sp` = `x2` = 00010
   - Immediate = 16 = `0000000000010000`

   **32-bit representation:**
   ```
   0000000000010000_00010_000_00010_0010011
   ```

7. **Instruction at address 0x1000c8:**
   ```
   JAL ra, -8
   ```
   - Type: J-Type
   - Opcode: 1101111
   - `rd` = `ra` = `x1` = 00001
   - Offset = -8 (signed 20-bit)

   **32-bit representation:**
   ```
   11111111111111111111_00001_1101111
   ```

8. **Instruction at address 0x1000cc:**
   ```
   RET
   ```
   - Pseudoinstruction for `JALR x0, x1, 0`
   - Type: I-Type
   - Opcode: 1100111
   - `rd` = `x0` = 00000
   - `rs1` = `x1` = 00001
   - Immediate = 0 = `000000000000`

   **32-bit representation:**
   ```
   000000000000_00001_000_00000_1100111
   ```

9. **Instruction at address 0x1000d0:**
   ```
   SUB x3, x4, x5
   ```
   - Type: R-Type
   - Opcode: 0110011
   - `rd` = `x3` = 00011
   - `rs1` = `x4` = 00100
   - `rs2` = `x5` = 00101
   - `func3` = 000
   - `func7` = 0100000

   **32-bit representation:**
   ```
   0100000_00101_00100_000_00011_0110011
   ```

10. **Instruction at address 0x1000d4:**
   ```
   OR x7, x8, x9
   ```
   - Type: R-Type
   - Opcode: 0110011
   - `rd` = `x7` = 00111
   - `rs1` = `x8` = 01000
   - `rs2` = `x9` = 01001
   - `func3` = 110
   - `func7` = 0000000

   **32-bit representation:**
   ```
   0000000_01001_01000_110_00111_0110011
   ```

11. **Instruction at address 0x1000d8:**
   ```
   AND x13, x14, x15
   ```
   - Type: R-Type
   - Opcode: 0110011
   - `rd` = `x13` = 01101
   - `rs1` = `x14` = 01110
   - `rs2` = `x15` = 01111
   - `func3` = 111
   - `func7` = 0000000

   **32-bit representation:**
   ```
   0000000_01111_01110_111_01101_0110011
   ```

12. **Instruction at address 0x1000dc:**
   ```
   LW x20, 4(x21)
   ```
   - Type: I-Type
   - Opcode: 0000011
   - `rd` = `x20` = 10100
   - `rs1` = `x21` = 10101
   - Offset = 4 = `000000000100`
   - `func3` = 010

   **32-bit representation:**
   ```
   000000000100_10101_010_10100_0000011
   ```

13. **Instruction at address 0x1000e0:**
   ```
   SW x22, 8(x23)
   ```
   - Type: S-Type
   - Opcode: 0100011
   - `rs1` = `x23` = 10111
   - `rs2` = `x22` = 10110
   - Offset = 8 = `0000000001000`
   - Split Immediate: `imm[11:5] = 0000000`, `imm[4:0] = 01000`
   - `func3` = 010

   **32-bit representation:**
   ```
   0000000_10110_10111_010_01000_0100011
   ```

14. **Instruction at address 0x1000e4:**
   ```
   BEQ x24, x25, -4
   ```
   - Type: B-Type
   - Opcode: 1100011
   - `rs1` = `x24` = 11000
   - `rs2` = `x25` = 11001
   - Offset = -4 = `1111111111111100`
   - Split Immediate: `imm[12|10:5] = 111111, imm[4:1|11] = 111100`
   - `func3` = 000

   **32-bit representation:**
   ```
   111111_11001_11000_000_111100_1100011
   ```

15. **Instruction at address 0x1000e8:**
   ```
   AUIPC x26, 16
   ```
   - Type: U-Type
   - Opcode: 0010111
   - `rd` = `x26` = 11010
   - Immediate = 16 << 12 = `000000000000000000010000000000`

   **32-bit representation:**
   ```
   00000000000000000001_11010_0010111
   ```

</details>

-------------------------------------------------

<details>
<summary><b>Task 4:</b> Functional Simulation of RISC-V Core and observe the waveforms</summary>  
<br> 

### Install Required Things
**1. Install ```GTKwave``` waveform viewer**

*Use the following command to install GTKWave*  
```  
$ sudo apt update
$ sudo apt install gtkwave  
```

**2. Install ```Icarus Verilog``` open source tool for simulation**

*Use the following command to install Icarus Verilog*
```  
$ sudo apt-get install iverilog
```

![gtkwave and iverilog Installation](https://github.com/adithyarg/samsung-riscv/blob/5c538202438e6086e69d498de63dcf48f23a04f5/Task%20-%204/installed%20required%20things.png)


### Steps to perform functional simulation of RISCV  
1. Create a new directory with your name ```mkdir <your_name>```
2. Create two files by using ```touch``` command as ```adithya_rv32i.v``` and ```adithya_rv32i_tb.v```  
3. Copy the code from the reference github repo and paste it in your verilog and testbench files  
  
  
4. To run and simulate the verilog code, enter the following command:  
	```
	$ iverilog -o adithya_rv32i adithya_rv32i.v adithya_rv32i_tb.v
	$ ./adithya_rv32i
	```
5. To see the simulation waveform in GTKWave, enter the following command:
	```
	$ gtkwave adithya_rv32i.vcd
	```


6. The GTKWave will be opened and following window will be appeared  
  
![4](https://github.com/adithyarg/samsung-riscv/blob/5fed5b8f5663158db8a9c37ec9ab2a20cba97e0c/Task%20-%204/gtk%20waveform.png)

#### *Analysing the Output Waveform of various instructions that we have covered in TASK-3*  
**```Instruction 1: ADD R6, R2, R1```**  
  
![ADD](https://github.com/adithyarg/samsung-riscv/blob/a47f56cbfc3dee9520abf9f6d26479c327a7b411/Task%20-%204/instruction%201.png)

**```Instruction 2: SUB R7, R1, R2```**  
  
![SUB](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%202.png)

**```Instruction 3: AND R8, R1, R3```**  

![AND](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%203.png)

**```Instruction 4: OR R9, R2, R5```**  

![OR](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%204.png)

**```Instruction 5: XOR R10, R1, R4```**  

![XOR](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%205.png)

**```Instruction 6: SLT R1, R2, R4```**  

![SLT](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%206.png)

**```Instruction 7: ADDI R12, R4, 5```**  

![ADDI](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%207.png)

**```Instruction 8: BEQ R0, R0, 15```**  
  
![BEQ](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%208.png)
 
**```Instruction 9: BNE R0, R1, 20```**

![BNE](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%209.png)
  
**```Instruction 10: SLL R15, R1, R2```**  

![SLL](https://github.com/adithyarg/samsung-riscv/blob/396f8d89e54316e2b8ad9b6a2d1cffab19c142a1/Task%20-%204/instruction%2010.png)


</details>

-------------------------------------------------

<details>
<summary><b>Task 5:</b> Task 5 of this internship is to Implementing an Energy Monitoring & Automation System Using VSD Squadron Mini CH32V003X</summary>  
  
## Implementing an Energy Monitoring & Automation System using VSDSquadron Mini  
  
### **Overview**  
This project implements a Smart Energy Monitoring & Automation System using the VSD Squadron Mini CH32V003X, a RISC-V-based SoC development kit. The system is designed to monitor voltage, current, power, and temperature in real-time, enabling efficient energy tracking and automated motor control.

The VSD Squadron Mini collects data from sensors, including a Voltage Sensor (25V), ACS712 Current Sensor, and DHT22 Temperature Sensor. It processes the data and transmits it via UART to an ESP32, which hosts a local web server for real-time visualization of energy parameters. The web dashboard displays live voltage, current, power, temperature, and energy consumption, along with a remote control option for the motor.

The relay module, controlled by the VSD Squadron. This project integrates hardware and software to demonstrate practical embedded system applications in energy management, automation, and IoT using RISC-V microcontrollers.
  
### **Components Required**  
* VSD Squadron Mini CH32V003X – RISC-V-based SoC development kit for processing and control  
* Voltage Sensor (25V) – Measures the input voltage to monitor energy consumption  
* ACS712 Current Sensor – Measures the current drawn by the motor 
* DHT22 Temperature Sensor – Monitors motor temperature to prevent overheating
* ESP32 – Hosts a local web server to display real-time data and enable remote control
* Relay Module – Controls motor operation based on temperature threshold
* DC Motor – The load whose energy parameters are being monitored
* 9V Battery – Provides power to the motor and circuit 
* Jumper Wires – For making necessary connections on the breadboard
* Breadboard – For circuit prototyping
* USB-to-Serial Adapter – For programming and debugging the VSD Squadron Mini  
* VS Code for Software Development  
* PlatformIO Multi-framework professional IDE for simulating and uploading code to the VSDSquadron Mini.
* HTML, CSS, and JavaScript – For designing the ESP32 web dashboard
  
### **Circuit Connections**  
* **Input:** Voltage, Current, and Temperature sensors are connected to the VSD Squadron Mini for real-time monitoring. 
* **Processing:** The VSD Squadron Mini calculates the sensor values and transmits the data to the ESP32 via UART. 
* **Output:** The ESP32 hosts a web dashboard displaying live sensor data and provides a remote control button for the relay. 
* **Relay Control:** The relay module is controlled by the VSD Squadron Mini based on temperature thresholds.

| Component                  | Pin Number  |
|----------------------------|-------------|
| Voltage Sensor (VCC)       | 5V          |
| Voltage Sensor (OUT)       | PC0         |
| Current Sensor (VCC)       | 5V          |
| Current Sensor (OUT)       | PC1         |
| Temperature Sensor (DHT22) | PC2         |
| ESP32 UART TX              | RX (PD6)    |
| ESP32 UART RX              | TX (PD5)    |
| Relay Module IN            | PD3         |
| Motor Positive Terminal    | Relay NO    |
| Motor Negative Terminal    | GND         |
  
![Energy Monitoring & Automation System](https://github.com/adithyarg/samsung-riscv/blob/dd8637262493cb75cde414f96b2e215d6c1125ad/Task%20-%205/Circuit%20Diagram%202.0.jpg)

**Explanation:**
- The system takes input from voltage, current, and temperature sensors.
- The VSDSquadron Mini processes these sensor values and transmits data to the ESP32 via UART communication.
- The ESP32 hosts a local web server, displaying real-time data on a dashboard.
- The dashboard shows Voltage, Current, Power, Temperature, and Energy Consumption over time.
- A threshold mechanism is implemented:
- Temperature Threshold: If the battery overheats, the system manual switch option of the motor through the web interface.
- Voltage and Current Monitoring: Used for energy calculations but does not trigger a shutdown.
- The relay module is controlled by the VSDSquadron Mini, allowing remote ON/OFF switching of the motor through the web interface.

---

</details>

--------------------------------------------------------------

<details>
<summary><b>Task 6:</b> Energy Monitoring & Automation with VSD Squadron Mini</summary>  

### **Introduction** 
This project focuses on developing a Smart Energy Monitoring & Automation System using the VSD Squadron Mini CH32V003X, a powerful RISC-V-based SoC development kit. The system is engineered to track voltage, current, power, and temperature in real-time, ensuring precise energy monitoring and intelligent motor automation.

By leveraging the VSD Squadron Mini, this system provides reliable data acquisition from various sensors and transmits the collected information to an ESP32, which acts as a local web server for real-time visualization. The system also features manual motor control via a relay module, ensuring safety by preventing overheating.

### **System Architecture** 
**1. Data Acquisition**
* Voltage Sensor (25V): Monitors real-time voltage levels to assess power consumption.
* ACS712 Current Sensor: Measures the electrical current drawn by the motor, helping to calculate power usage.
* DHT22 Temperature Sensor: Monitors ambient temperature near the motor to prevent overheating.

**2. Processing Unit**
* The VSD Squadron Mini CH32V003X reads sensor values and processes them efficiently.
* It transmits the processed data via UART communication to the ESP32 for further use.

**3. Web Dashboard & Data Visualization**
* The ESP32 functions as a web server, allowing users to monitor energy parameters through a custom-built dashboard.
* The dashboard, developed using HTML, CSS, and JavaScript, displays real-time graphs and sensor readings, including
- Voltage
- Current
- Power Consumption
- Temperature
- Energy Consumption Over Time
  
### How to Program for VSD Squadron Mini Board?  
```
 #include <stdio.h>
 #include <string.h>      // For strlen, strstr, memset
 #include <ch32v00x.h>    // Adjust as needed for your SDK
 #include <debug.h>       // Delay functions, etc.
 
 /* Pin Definitions (adjust to your setup) */
 #define RELAY_PIN       GPIO_Pin_0      // PC0 for Relay
 #define RELAY_GPIO_PORT GPIOC
 
 /* Function Prototypes */
 void System_Init(void);
 void GPIO_Config(void);
 void ADC_Config(void);
 void UART_Config(void);
 uint16_t ADC_ReadValue(uint8_t channel);
 void sendDataOverUART(float voltage, float current, float temperature);
 void checkForRelayCommand(void);
 
 /* Globals for sensor values */
 volatile float g_voltage = 0.0f;
 volatile float g_current = 0.0f;
 volatile float g_temperature = 0.0f;
 
 int main(void)
 {
     /* Initialization */
     NVIC_PriorityGroupConfig(NVIC_PriorityGroup_1);
     SystemCoreClockUpdate();
     Delay_Init();
     GPIO_Config();
     ADC_Config();
     UART_Config();
 
     while(1)
     {
         // Read ADC values from channels 0, 1, 2
         uint16_t rawVoltage = ADC_ReadValue(0);  // e.g. ADC channel 0 -> PD0
         uint16_t rawCurrent = ADC_ReadValue(1);  // e.g. ADC channel 1 -> PD1
         uint16_t rawTemp    = ADC_ReadValue(2);   // e.g. ADC channel 2 -> PD2
 
         // Convert raw ADC values to engineering units (adjust scaling as needed)
         g_voltage     = (rawVoltage * 3.3f / 1023.0f) * (9.0f / 3.3f);  // Example scaling for 9V battery
         g_current     = (rawCurrent * 3.3f / 1023.0f) * 2.0f;            // Example scaling for current sensor
         g_temperature = (rawTemp * 3.3f / 1023.0f) * 100.0f;             // Example scaling for temperature sensor
 
         // Send sensor data over UART to ESP32
         sendDataOverUART(g_voltage, g_current, g_temperature);
 
         // Check for incoming relay control commands
         checkForRelayCommand();
 
         // Delay before next reading
         Delay_Ms(500);
     }
 }
 
 /* System/Clock Initialization */
 void System_Init(void)
 {
     SystemCoreClockUpdate();
     /* Enable clocks for GPIO/ADC/UART, etc. */
     RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);
     RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC, ENABLE);
     RCC_APB2PeriphClockCmd(RCC_APB2Periph_ADC1, ENABLE);
     RCC_APB2PeriphClockCmd(RCC_APB2Periph_AFIO, ENABLE);
 }
 
 /* Configure GPIO for ADC inputs and Relay output */
 void GPIO_Config(void)
 {
     GPIO_InitTypeDef GPIO_InitStructure;
 
     /* ADC Pins: PD0, PD1, PD2 as analog input */
     GPIO_InitStructure.GPIO_Pin = GPIO_Pin_0 | GPIO_Pin_1 | GPIO_Pin_2;
     GPIO_InitStructure.GPIO_Mode = GPIO_Mode_AIN;
     GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz; 
     GPIO_Init(GPIOD, &GPIO_InitStructure);
 
     /* Relay Pin: PC0 as push-pull output */
     GPIO_InitStructure.GPIO_Pin = RELAY_PIN;
     GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
     GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
     GPIO_Init(RELAY_GPIO_PORT, &GPIO_InitStructure);
 
     /* Set relay off initially */
     GPIO_ResetBits(RELAY_GPIO_PORT, RELAY_PIN);
 }
 
 /* Configure ADC */
 void ADC_Config(void)
 {
     ADC_InitTypeDef ADC_InitStructure;
 
     ADC_DeInit(ADC1);
     ADC_InitStructure.ADC_Mode = ADC_Mode_Independent;
     ADC_InitStructure.ADC_ScanConvMode = DISABLE;        // single channel mode
     ADC_InitStructure.ADC_ContinuousConvMode = DISABLE;    // single conversion
     ADC_InitStructure.ADC_ExternalTrigConv = ADC_ExternalTrigConv_None;
     ADC_InitStructure.ADC_DataAlign = ADC_DataAlign_Right;
     ADC_InitStructure.ADC_NbrOfChannel = 1;
     ADC_Init(ADC1, &ADC_InitStructure);
 
     ADC_Cmd(ADC1, ENABLE);
 
     // Calibration
     ADC_ResetCalibration(ADC1);
     while(ADC_GetResetCalibrationStatus(ADC1));
     ADC_StartCalibration(ADC1);
     while(ADC_GetCalibrationStatus(ADC1));
 }
 
 /* Read one ADC channel */
 uint16_t ADC_ReadValue(uint8_t channel)
 {
     // Configure the channel with a sample time (using ADC_SampleTime_43Cycles)
     ADC_RegularChannelConfig(ADC1, channel, 1, ADC_SampleTime_43Cycles);
     ADC_SoftwareStartConvCmd(ADC1, ENABLE);
     while(!ADC_GetFlagStatus(ADC1, ADC_FLAG_EOC))
     {
         // wait for conversion to complete
     }
     return ADC_GetConversionValue(ADC1);
 }
 
 /* Configure UART (PD5=TX, PD6=RX) */
 void UART_Config(void)
 {
     GPIO_InitTypeDef GPIO_InitStructure;
     USART_InitTypeDef USART_InitStructure;
 
     /* Enable USART1 clock */
     RCC_APB2PeriphClockCmd(RCC_APB2Periph_USART1, ENABLE);
 
     /* Configure TX Pin (PD5) */
     GPIO_InitStructure.GPIO_Pin = GPIO_Pin_5;
     GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
     GPIO_InitStructure.GPIO_Mode = GPIO_Mode_AF_PP;
     GPIO_Init(GPIOD, &GPIO_InitStructure);
 
     /* Configure RX Pin (PD6) */
     GPIO_InitStructure.GPIO_Pin = GPIO_Pin_6;
     GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IN_FLOATING;
     GPIO_Init(GPIOD, &GPIO_InitStructure);
 
     /* UART configuration: 115200 baud, 8N1 */
     USART_InitStructure.USART_BaudRate = 115200;
     USART_InitStructure.USART_WordLength = USART_WordLength_8b;
     USART_InitStructure.USART_StopBits = USART_StopBits_1;
     USART_InitStructure.USART_Parity = USART_Parity_No;
     USART_InitStructure.USART_HardwareFlowControl = USART_HardwareFlowControl_None;
     USART_InitStructure.USART_Mode = USART_Mode_Rx | USART_Mode_Tx;
     USART_Init(USART1, &USART_InitStructure);
 
     USART_Cmd(USART1, ENABLE);
 }
 
 /* Send sensor data over UART in text format */
 void sendDataOverUART(float voltage, float current, float temperature)
 {
     char buffer[64];
     sprintf(buffer, "VOL=%.2f,CUR=%.2f,TMP=%.2f\n", voltage, current, temperature);
 
     for(uint8_t i = 0; i < strlen(buffer); i++)
     {
         while(USART_GetFlagStatus(USART1, USART_FLAG_TXE) == RESET);
         USART_SendData(USART1, buffer[i]);
     }
 }
 
 /* Check for incoming relay commands from ESP32 */
 void checkForRelayCommand(void)
 {
     static char rxBuffer[32];
     static uint8_t idx = 0;
 
     while(USART_GetFlagStatus(USART1, USART_FLAG_RXNE) == SET)
     {
         char c = (char)USART_ReceiveData(USART1);
         if(c != '\n' && idx < sizeof(rxBuffer) - 1)
         {
             rxBuffer[idx++] = c;
         }
         else
         {
             rxBuffer[idx] = '\0';
             if(strstr(rxBuffer, "RELAY=ON"))
             {
                 GPIO_SetBits(RELAY_GPIO_PORT, RELAY_PIN);  // Turn relay on
             }
             else if(strstr(rxBuffer, "RELAY=OFF"))
             {
                 GPIO_ResetBits(RELAY_GPIO_PORT, RELAY_PIN); // Turn relay off
             }
             idx = 0;
             memset(rxBuffer, 0, sizeof(rxBuffer));
         }
     }
 }
 


```


### How to Program for ESP 32 Board?  
```
#include <WiFi.h>
#include <WebServer.h>

// Replace with your network credentials:
const char* ssid = "Your_SSID";
const char* password = "Your_PASSWORD";

// Global sensor values
float g_voltage = 0.0;
float g_current = 0.0;
float g_temperature = 0.0;

// Create a web server object on port 80
WebServer server(80);

// Function prototypes
void handleRoot();
void handleMotorOn();
void handleMotorOff();
void updateSensorDataFromSerial();
void parseSensorData(const String &dataLine);

void setup() {
  Serial.begin(115200); // Ensure this baud rate matches the VSD board's UART rate
  delay(1000);

  // Connect to WiFi
  WiFi.begin(ssid, password);
  Serial.println("Connecting to WiFi...");
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println();
  Serial.print("WiFi connected. IP address: ");
  Serial.println(WiFi.localIP());

  // Define URL routes
  server.on("/", handleRoot);
  server.on("/motor/on", handleMotorOn);
  server.on("/motor/off", handleMotorOff);
  
  // Start the web server
  server.begin();
  Serial.println("Web server started.");
}

void loop() {
  server.handleClient();
  updateSensorDataFromSerial();
}

/* Web page: Displays sensor data and relay control buttons */
void handleRoot() {
  String html = R"rawliteral(
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <title>Energy Monitoring Dashboard</title>
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
      <style>
        body {
          background: #2c3e50;
          color: #ecf0f1;
          font-family: 'Roboto', sans-serif;
        }
        .card {
          background: #34495e;
          border: none;
          margin-top: 30px;
          box-shadow: 0 4px 6px rgba(0,0,0,0.4);
        }
        .card-header {
          background: #1abc9c;
          border-bottom: 1px solid #16a085;
        }
        .sensor-value {
          font-size: 2rem;
          font-weight: bold;
        }
        .sensor-label {
          font-size: 1rem;
          opacity: 0.9;
        }
        .btn-custom {
          background: #e67e22;
          border: none;
          font-size: 1.2rem;
          padding: 10px 20px;
          color: #ffffff;
        }
        .btn-custom:hover {
          background: #d35400;
        }
      </style>
    </head>
    <body>
      <div class="container">
        <div class="card">
          <div class="card-header text-center">
            <h2>Energy Monitoring Dashboard</h2>
          </div>
          <div class="card-body">
            <div class="row text-center">
              <div class="col-md-3 mb-3">
                <div class="sensor-label">Temperature</div>
                <div id="temperature" class="sensor-value">-- °C</div>
              </div>
              <div class="col-md-3 mb-3">
                <div class="sensor-label">Voltage</div>
                <div id="voltage" class="sensor-value">-- V</div>
              </div>
              <div class="col-md-3 mb-3">
                <div class="sensor-label">Current</div>
                <div id="current" class="sensor-value">-- A</div>
              </div>
              <div class="col-md-3 mb-3">
                <div class="sensor-label">Power</div>
                <div id="power" class="sensor-value">-- W</div>
              </div>
            </div>
            <div class="text-center">
              <button class="btn btn-custom" onclick="toggleRelay()">Toggle Relay</button>
            </div>
          </div>
        </div>
      </div>
      
      <script>
        function fetchSensorData() {
          fetch('/sensor')
            .then(response => response.json())
            .then(data => {
              document.getElementById('temperature').innerText = data.temperature.toFixed(2) + ' °C';
              document.getElementById('voltage').innerText = data.voltage.toFixed(2) + ' V';
              document.getElementById('current').innerText = data.current.toFixed(2) + ' A';
              document.getElementById('power').innerText = data.power.toFixed(2) + ' W';
            })
            .catch(err => console.error('Error fetching sensor data:', err));
        }

        function toggleRelay() {
          fetch('/toggle')
            .then(response => response.text())
            .then(() => fetchSensorData())
            .catch(err => console.error('Error toggling relay:', err));
        }

        setInterval(fetchSensorData, 3000);
        window.onload = fetchSensorData;
      </script>
    </body>
    </html>
  )rawliteral";
  server.send(200, "text/html", html);
}

/* Turn motor off: Send command to VSD board and redirect back */
void handleMotorOff() {
  Serial.println("RELAY=OFF");
  server.sendHeader("Location", "/");
  server.send(303);
}

/* Read incoming serial data and update sensor values */
void updateSensorDataFromSerial() {
  static String serialLine = "";
  while (Serial.available() > 0) {
    char c = (char)Serial.read();
    if (c == '\n') {
      // When a full line is received, parse it.
      parseSensorData(serialLine);
      serialLine = "";
    } else {
      serialLine += c;
    }
  }
}

/* Parse sensor data formatted as "VOL=xx.xx,CUR=yy.yy,TMP=zz.zz" */
void parseSensorData(const String &dataLine) {
  int idxVol = dataLine.indexOf("VOL=");
  int idxCur = dataLine.indexOf("CUR=");
  int idxTmp = dataLine.indexOf("TMP=");
  
  if (idxVol != -1 && idxCur != -1 && idxTmp != -1) {
    String volStr = dataLine.substring(idxVol + 4, dataLine.indexOf(',', idxVol));
    String curStr = dataLine.substring(idxCur + 4, dataLine.indexOf(',', idxCur));
    int commaPos = dataLine.indexOf(',', idxTmp);
    String tmpStr = (commaPos == -1) ? dataLine.substring(idxTmp + 4) 
                                     : dataLine.substring(idxTmp + 4, commaPos);

    g_voltage = volStr.toFloat();
    g_current = curStr.toFloat();
    g_temperature = tmpStr.toFloat();
  }
}



``` 

### Working Video  
[Video Link](https://drive.google.com/drive/folders/1jLbWHpoGpOX7e65LjiXLVVcyqz6CiS4_?usp=sharing)

</details>

--------------------------------------------------------------

