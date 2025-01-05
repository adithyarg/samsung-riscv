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
<summary><b>Task 1:</b> Task 1: Installation of RISC-V Toolchain and Lab Setup</summary>   
<br>

**1. Install Ubuntu 20.04 LTS on Oracle Virtual Machine Box**

![Ubuntu and VMBox Installation](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/11c35aff-f587-40f5-a7d2-683dbf0784d4)

**2. Install RISC-V [GNU ToolChain](https://github.com/riscv-collab/riscv-gnu-toolchain)**

### What is RISC-V GNU Toolchain?
> The RISC-V GNU Compiler Toolchain is a free and open source cross-compiler for C and C++. It supports two build modes: Generic ELF/Newlib and Linux-ELF/glibc. The toolchain can be used to create assembly instructions and sequences for execution in a simulator and target FPGA  

*Use the following command to install GNU Toolchain*
```  
$ sudo apt install git  
$ git clone https://github.com/riscv/riscv-gnu-toolchain
$ sudo apt-get install autoconf automake autotools-dev curl python3 python3-pip libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev ninja-build git cmake libglib2.0-dev libslirp-dev  
$ mkdir /opt/riscv
$ ./configure --prefix=/opt/riscv --with-arch=rv64i --with-abi=lp64 --enable-multilib
$ sudo make
```
Now add ```/opt/riscv/bin``` to **PATH**  
```
$ gedit ~/.bashrc  
````  
Add the line ```export PATH="$PATH:/opt/riscv/bin"``` in the end of file and save it. After that run the following command:  
```
$ source ~/.bashrc
```

![RISC-V GNU Toolchain Installation](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/2ca2294c-28f5-43dd-bf9d-41abf33c9d02)

**3. Install ```Yosys Open SYnthesis Suite```**

### What is Yosys?
> Yosys, or Yosys Open SYnthesis Suite, is a free, open-source framework for Verilog RTL synthesis. It can be used to process almost any synthesizable Verilog-2005 design, and to convert Verilog to BLIF, EDIF, BTOR, SMT-LIB, and more. Yosys can be customized to perform any synthesis job by combining the existing passes (algorithms) using synthesis scripts and adding additional passes as needed by extending the yosys C++ code base  
  
*Use the following command to install Yosys*
```  
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make //If make is not installed, make sure to install it first
$ sudo apt-get install build-essential clang bison flex \
	libreadline-dev gawk tcl-dev libffi-dev git \
	graphviz xdot pkg-config python3 libboost-system-dev \
	libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make 
$ sudo make install  
```

![Yosys Installation](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/a6c0eddb-fad4-4cd2-8bf6-7f4bc2b20b22)

**4. Install ```GTKwave``` waveform viewer**

### What is GTKWave?
> GTKWave is a free, lightweight waveform viewer that's used to display simulation output. It's based on the GTK library and supports VCD and LXT formats for signal dumps. A waveform viewer that allows for the visualization of simulation outputs, facilitating the analysis of digital signals.  

*Use the following command to install GTKWave*  
```  
$ sudo apt update
$ sudo apt install gtkwave  
```

![gtkwave Installation](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/11156322-7ae3-4cea-9e09-b7952764df28)

**5. Install ```Icarus Verilog``` open source tool for simulation**

### What is iverilog?  
> Icarus Verilog is a compiler for the Verilog hardware description language (HDL). It's used to collect Verilog source code, check for errors, and write compiled design files. It also helps access source files in libraries, link modules, and write compiled results  

*Use the following command to install Icarus Verilog*
```  
$ sudo apt-get install iverilog
```

![iverilog Installation](https://github.com/maazm007/vsdsquadron-mini-internship/assets/83294849/0c3be648-2f4f-48d3-bb53-45bfc56ba9b2)
</details>

------------------------------------------------------------------------------------------------------------------
