# From Bit to Program Computer

This is a collection of programs and files that will be explained as you follow the various projects. It's used to implementing projects and theory in book [The Elements of Computing Systems: Building a Modern Computer from First Principles](https://www.amazon.com/Elements-Computing-Systems-Building-Principles/dp/0262640686/ref=ed_oe_p) of **[Prof. Noam Nisan](http://www.cs.huji.ac.il/~noam/)** work at the Institute of Computer Science and Engineering, Hebrew University of Jerusalem and **[Prof. Shimon Schocken](https://www.shimonschocken.com/)** . And the project **From Bit to Program Computer** referenced from the [this book](https://www.amazon.com/Elements-Computing-Systems-Building-Principles/dp/0262640686/ref=ed_oe_p) and after author of **From Bit to Program Computer** deep research more for [this project](https://github.com/fulstat/From-Bit-to-Program-Computer).   

The Software Tools in file involved the following software:
+ **Hardware Simulator**: [Guide Document](/Tutorial/hardware-simulator.md) 

Simulates and tests logic gates and chips implemented in the HDL (Hardware Description Language) described in the book. Used in hardware construction projects.
+ **CPU Emulator**: [Guide Document](/Tutorial/cpu-simulator.md) 

Emulates the operation of the Hack computer system. Used to test and run programs written in the Hack machine language (Hack computer is 16 bit machine, belong to Havard architecture and is different from Hack is a programming language for the HipHop Virtual Machine, created by Facebook), in both its binary and assembly versions.
+ **VM Emulator**: [Guide Document](/Tutorial/vm-emulator.md) 

Emulates the operation of our virtual machine (similar to Java's JVM); used to run and test programs written in the VM language (similar to Java's Bytcode).
+ **Assembler**: [Guide Document](/Tutorial/Assembler.md) 

Translates programs from the [Hack assembly language](http://www.marksmath.com/tecs/hack-asm/hack-asm.html) to Hack binary code. The resulting code can be executed directly on the Computer chip (in the hardware simulator), or emulated on the supplied CPU Emulator (much faster and more convenient).
+ **Compiler**: 
Translates programs written in [Jack](https://classes.engineering.wustl.edu/cse365/jack.php) (a simple, Java-like object-based language) into VM code. 
+ Operating system:
Two OS implementations are supplied: (i) **a collection of eight .vm class files, written originally in [Jack](https://classes.engineering.wustl.edu/cse365/jack.php)** (just like Unix is written in C), and (ii) a faster implementation of all the OS services, embedded in the supplied VM Emulator.
+ **Text Comparer**

### Install in Mac OS:
#### Install Java for Mac

##### Java 8:

```
brew tap caskroom/versions
brew cask install java8
```
##### Java 9:
```
brew cask install java
```

After installing Java, verify the installation by starting a new Terminal window and typing `java -version`

#### Install the Software Suite:
Double-click the .zip file you've downloaded from the host. OS X will automatically extract the contents of the .zip file to a folder. Move this folder to your desktop.

To run any one of the tools on OS X, you must use the command line. Start the Terminal application (Applications - Utilities - Terminal). Once the terminal window appears, type the following:

`~/Desktop/tools/HardwareSimulator.sh`

All the supplied software tools are started in a similar way: just replace **HardwareSimulator** with the name of the software tool you wish to run.

Tools | **Command**
------|------------
Hardware Simulator	| HardwareSimulator.sh
CPU Emulator	| CPUEmulator.sh
Assembler	| Assembler.sh
VM Emulator	| VMEmulator.sh
Jack Compiler	| JackCompiler.sh

To run any software, replacing **Command** with one of the commands listed above:

`~/Desktop/tools/Command`

### Install in Windows:
#### Install Java:

[Click here](https://www3.ntu.edu.sg/home/ehchua/programming/howto/JDK_Howto.html)

### Install in Ubuntu:
#### Install Java:
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

___The supplied software tools are ran from your computer's command-line environment (also known as "terminal", or "shell"). Command-line environments vary from one operating system to another, and working in them requires some knowledge of various OS shell commands.___

___For Mac and Linux users:___
If you want to avoid typing the 'sh' extensions, you can create (once and for all) symbolic links in your ~/bin directory. Here example the HardwareSimulator tool:

```
ln -s ~/tools/HardwareSimulator.sh HardwareSimulator
chmod +x HardwareSimulator
```
___For Windows users:___
For the batch files to work from the command line, you must add (once and for all) the /tools_directory to your **PATH variable** to setup environment variables.

To run a batch file from command-line, type its **name**, without the .bat extension.
You can create desktop icons and use them to invoke the interactive versions of the following supplied tools: **HardwareSimulator, Assembler, CPUEmulator and VMEmulator**. 


