# "Hello, World!" in RISC-V (Reduced Instruction Set Computing - 5)

RISC-V is an open-source instruction set architecture (ISA):

- Anyone can implement, modify, and use the architecture without having to pay royalties or licensing fees. Intel and ARM are considered proprietary.

- Designed to be simple and modular with a base set of instructions that can be extended to meet specific needs.


*** 
## Configuration

Here is how I configured my Linux Mint environment to interpret these instructions
1. Installed the necessary toolchain:
   **apt install gcc-riscv64-linux-gnu**

2. Create a Makefile. This is what my Makefile looks like:
   ```Makefile
   rm -rf hello
   riscv64-linux-gnu-as hello.s -o hello.o
   riscv64-linux-gnu-gcc hello hello.o -nostdlib -static
   ```

3. Use the command "Make" in your terminal to invoke the Makefile.

4. To run the hello.o file created by invoking the Makefile, you can either use **"./hello"** or **"qemu-riscv64 ./hello"**.


        