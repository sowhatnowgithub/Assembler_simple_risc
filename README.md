# 🛠️ Assembler for Simple RISC
Welcome to the **Simple RISC Assembler**, an open-source assembler written in **C** for a custom Reduced Instruction Set Computing (RISC) architecture. This project enables **tokenization, validation, and encoding of assembly instructions** into machine-readable formats.


## HOW TO USE THIS

## Prerequisites
### I have tested this code on mac m2, it works fine, hoping its the same to you as well ☺️☺️😅😅

Before starting, you need to have the following installed on your machine:

1. **GCC Compiler**: This is required to compile the C code.
2. 
   - You can install GCC on Linux using the following command:
     ```bash
     sudo apt-get install build-essential
     ```
   - On macOS, you can install it through Homebrew:
     ```bash
     brew install gcc
     ```

3. **Git** (Optional): If you want to clone the repository directly.

## Setting Up the Project

### Option 1: Clone the Repository Using Git

If you have Git installed, you can clone the repository directly by running the following command:

```bash
git clone https://github.com/sowhatnowgithub/Assembler_simple_risc.git

```
### Option 2: Download the ZIP File

If you don't have Git installed, you can download the ZIP file from the repository's page:

-Navigate to the repository on GitHub.

-Click the "Code" button on the right side.

-Select "Download ZIP."

After downloading or cloning, you will have the source files required for the assembler in the Assembler_simple_risc directory.

Now navigate to the **dev** folder in **Assembler_simple_risc**.

There you will see all the source c files.

## Creating and Compiling Your Own Assembly Program

### Step 1: Create Your Assembly File

Create your own assembly program using a text file with the .txt extension
(e.g., my_program.txt). Place this file in the project directory.
I have given few examples programs named asm.txt, asm1.txt. Now you can use them for testing.
### Step 2: Compile the Program
Once you have the assembly file ready, compile the source files using the following command: 
```
gcc -o main main.c 
```
The above command will createa a executable main, which is already present in the dev folder, doing this won't affect the main executable, unless you change the main.c or any other files like token_parser.c or instruction_encoder.c these are important for the execution don't change them, unless you want to play with them 👩‍💻.

### Step 3: Execute the Assembler
To execute the assembler with your program, use the following command:
```
./main assembly_program.txt
```
## You have to pass the program file as argument for the execution or else it will throw error

## Expected Output
Once the program starts execution, you will see the tokenization process happening. If there are any errors in the code, they will be displayed during tokenization.

### Step 4: Generate Binary and Integer Files
After tokenization, the program will prompt you to enter a file name for the binary and integer files to be generated. Do not include an extension when entering the file name, as the program will automatically append the appropriate extension.

### Step 5: View the Generated Files
Once the files are generated, the program will stop execution. You can find the generated files (with .bin and .int extensions) in the current working directory.


## 🚀 Project Overview
This assembler **translates Simple RISC assembly code** into integer-based binary representations, ensuring accurate instruction processing and validation.

### 🔍 Features

✅ **Instruction Parsing & Tokenization**

✅ **You can use label declaration any where as long as, it is following rules, see live documentation (please scroll down you will find it)**

✅ **It does not care about white space, but new line (\n) are treated as new instructions, so be careful to complete the instruction in one line, and use new line for a new instruction**

✅ **Instruction Parsing & Tokenization**

✅ **Register & Label Handling**

✅ **It will identify errors in immediate or label mismatch, register validation and all mentioned properties in documentation**

✅ **Binary equivalent integer file generation**

✅ **Binary File Generation**

✅ **GUI Assembler (Work in Progress 🚧)**

✅ **You can add hlt at the end to specify end of program, but its not needed**




---

## 📂 Project Structure
----------------------------------------

    ├── README.md             # 📖 Project Documentation

    ├── index.html            # 🌐 Web-based documentation (Hosted on GitHub Pages)

    ├── main.css              # 🎨 Styling for the documentation

    └── dev/

        ├── main.c            # 🏗️ Contains the main() function
    
        ├── token_parse.c     # 🔍 Handles tokenization & input validation
    
        ├── tokens.h          # 🏷️ Header file for tokens
    
        ├── instruction_encoder.c  # 🛠️ Converts tokens to integer representations
        
        ├── out.int           # 📜 Integer-encoded instructions
    
        ├── asm.txt           # 📄 Sample assembly code
    
        ├── asm1.txt          # 📄 Additional sample code
    
        ├── main              # 🔧 Compiled binary


----------------------------------------

# 🔢 Instruction Encoding Format

The out.int file contains integer-encoded instructions based on the following format:

```
Assembly Instruction:   add r15, r2, 0x12
Integer Encoding:       0|1|15|2|0|18
```

- **Binary Encoding:** This is a 32 bit encoding for each instruction.

- **Opcode Mapping:** Each instruction is assigned a unique integer opcode.
  
- **Register Encoding:** Registers (`rX`) are mapped to their respective
integer representations and X is in between 0-15.

- **Immediate Values:** Hex values (e.g., `0x12`) are converted to their decimal equivalents.

---

## 🛠️ Assembler Workflow

1️⃣ **Tokenization & Validation** (`token_parse.c`)
- Extracts tokens from assembly code
- Validates registers, operands, and syntax
- 

2️⃣ **Instruction Encoding** (`instruction_encoder.c`)
- Maps tokens to corresponding integer values
- Converts labels and immediate values into their respective formats
- 

3️⃣ **Binary File Generation** (`out.int`)
- Stores machine-readable instruction sequences

---

## 🔗 Live Documentation
📖 **[View Online Documentation](https://sowhatnowgithub.github.io/Assembler_simple_risc/)**

If you haven't visited our hosted documentation, please **check the main rules and implementation details** at the bottom of this README.

---

## 📜 Assembler Rules & Implementation Details


### 🏗 Development Guidelines

🔹 **Relative Addressing & ORG Handling**

🔹 **Opcode & Operand Validation**

🔹 **Register Addressing Modes**

🔹 **Label Mapping with Instruction Addresses**

🔹 **Immediate Value Formatting (e.g., `0x24h` format required)**

### ⚠️ Key Constraints

⚡ **The immediate value has to written in lowercase alphabets. ex:`0x12baf`** 

⚡ **The immediate value has to start with in `0x`, only `0x` is given then error will come** 

⚡ **Maximum Instructions:** `999`

⚡ **Character Limit (Excluding Whitespace):** `30,000`

⚡ **Label Length Limit:** `9 characters`

---

## 💡 How to Contribute

We **welcome** all contributions—whether it's fixing bugs, adding new features, or improving documentation.


🔧 **Ways to Contribute:**

✅ **Report Issues** – Found a bug? Open an issue!

✅ **Submit a PR** – Have a fix or enhancement? Send a pull request!

✅ **Improve Documentation** – Help keep our docs clear & concise!


Stay tuned for updates & new features! 🚀


---

⭐ **If you like this project, consider giving it a star!** 🌟

📌 **Maintained by:** *sowhatnow/sowhatnowgithub*
