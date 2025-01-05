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
1. Open the terminal and run the given command:  

	```
	cat sum_1ton.c
	```
![cat Command](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/a272d8d0-63e5-4f00-9899-2223402be21d)

2. Using the **cat** command, the entire C code will be displayed on the terminal. Now run the following command to compile the code in riscv64 gcc compiler:  

	```
	riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
	```
3. Open a new terminal and run the given command:    

	```
	riscv64-unknown-elf-objdump -d sum_1ton.o
	```
![Objdump using -O1 format](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/dbf50220-d897-4b69-b33d-d0201fddb4fb)

4. The Assembly Language code of our C code will be displayed on the terminal. Type ```/main``` to locate the main section of our code.  

### *Descriptions of the keyword used in above command*  
* **-mabi=lp64:** This option specifies the ABI (Application Binary Interface) to use ```lp64```, which is for 64-bit integer, long and pointer size. This ABI is used for 64-bit RISCV architecture.  
* **-march=rv64i:** This option specifies the architecture that we use, which is rv64i, indicates the 64-bit RISCV base integer instruction set. This also confirms the targeting of 64-bit architecture.  
* **riscv-objdump:** A tool for disassembling RISC-V binaries, providing insights into the code structure and helping in debugging.  
* **-Ofast:** The option -Ofast in the command ```riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c``` is a compiler optimization flag used with the GNU Compiler Collection (GCC). This flag is used to instruct the compiler to optimize the generated code for maximum speed. The use of ```-Ofast``` is typically chosen for applications where execution speed is critical and where deviations from standard behavior are acceptable. However, it's important to test thoroughly, as this level of optimization can introduce subtle bugs, especially in complex calculations or when strict compliance with external standards is required.  
* **-O1:** This options is an optimization level that tells the compiler to optimize the generated code but without greatly increasing compilation time. -O1 aims to reduce code size and execution time while keeping the compilation process relatively quick.  

#### *Other common options are as follows:*  
> 1. **-O0:** No optimization, the default level if no -O option is specified.  
> 2. **-O2:** More aggressive optimizations that might increase compilation time but typically provide faster and sometimes smaller code.  
> 3. **-O3:** Maximizes optimization more aggressively than -O2.  
> 4. **-Os:** Optimizes code for size. It enables all -O2 optimizations that do not typically increase code size.

Here, the term **more aggressive optimization** in the context of compilers like GCC refers to a deeper and more complex set of transformations applied to the code in order to improve its performance and possibly reduce its size. The compiler uses more complex techniques that aims to generate faster executing code or code that occupies less memory. However, these optimizations typically increase the compilation time and can sometimes introduce bugs, making it harder to debug.
</details>

-------------------------------------------------
