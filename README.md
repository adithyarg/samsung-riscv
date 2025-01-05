#  VSDSquadron-Mini Internship Program 2024-25

RISC-V Talent Development Program, powered by Samsung Semiconductor India Research (SSIR) along with VLSI System Design (VSD). The instructor for this internship is Kunal Ghosh Sir.

##  Basic Details

**Name:** Adithya  
**College:** Sahyadri College of Engineering and Management  
**Email ID:** adithyar.ec23@sahyadri.edu.in  
**GitHub Profile:** [Adithya](https://github.com/adithyarg?tab=repositories)  
**LinkedIn Profile:** [adithya-rg](https://www.linkedin.com/in/adithya-rg-74a23b293/)

----------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 1:</b> Installation of essential tools required for this internship such as Ubuntu on VMBox and refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler</summary>   
<br>

### Installed Ubuntu 18.04 LTS on Oracle Virtual Machine Box**
- Downloaded the RISC-V workshop VDI file.
- Installed Oracle VirtualBox and created a virtual machine with the following specifications:
  - **RAM:** 4 GB  
  - **CPU Cores:** 2  
  - **Operating System:** Linux-based Ubuntu 18.04 LTS
- Successfully set up the virtual environment and folder structure for further tasks.

![Ubuntu and VMBox Installation](https://github.com/adithyarg/samsung-riscv/blob/02f5373bd8c49656c3451b399060c7010b2eb032/Task%20-%201/Ubuntu%20and%20VMBox%20Installation.png)

---

### Created and Tested a given C Language based LAB**
We have to follow the given steps to compile any **.c** file in our machine:
1. Open the bash terminal and locate to the directory where you want to create your file. Then run the following command:

  ```bash
  $ cd
  $ sudo install leafpad
  $ leafpad sum1ton.c &
```
 2. This will open the editor and allows you to write into the file that you have created. You have to write the C code of printing the sum of n numbers. Once you are done with your code, press ```Ctrl + S``` to save your file, and then press ```Ctrl + W``` to close the editor.   

![Developed a C program.](https://github.com/adithyarg/samsung-riscv/blob/8d8861fddf455f28ee2bc3192204ddb8c48c007c/Task%20-%201/Code%20of%20C%20based%20lab.png)

3. To the C code on your terminal, run the following command:
  ```bash
  $ gcc sum1ton.c
  $ ./a.out
```
![Executed a C program.](https://github.com/adithyarg/samsung-riscv/blob/36ab2b1e17f4fd08f3da0d9146c3c4f1af4fd923/Task%20-%201/Execution%20of%20C%20based%20lab.png)

  
------------------------------------------------------------------------------------------------------------------

### RISCV based LAB
We have to do the same compilation of our code but this time using RISCV gcc compiler. Follow the given steps:  
1. Use the cat command to display the content of the sum1ton.c file in the terminal: 

	```
	cat sum_1ton.c
	```
![cat Command](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/a272d8d0-63e5-4f00-9899-2223402be21d)

2. Using the **cat** command, the entire C code will be displayed on the terminal. Compile with Optimization Level O1
Compile the code using the RISC-V GCC compiler with the following flags:

	```
	riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c

3. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	riscv64-unknown-elf-objdump -d sum1ton.o | less
	```
4. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.
![Objdump using -O1 format](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/dbf50220-d897-4b69-b33d-d0201fddb4fb)

5. Compile with Optimization Level Ofast, Compile the code using the RISC-V GCC compiler with the following flags:

	```
	riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

6. Open a new terminal and Generate the assembly language equivalent of the compiled object file using the objdump tool:    

	```
	riscv64-unknown-elf-objdump -d sum1ton.o | less
	```
7. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.
![Objdump using -O1 format](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/dbf50220-d897-4b69-b33d-d0201fddb4fb)

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
