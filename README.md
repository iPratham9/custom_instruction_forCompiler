# custom_instruction_forCompiler
 
🧠 PrathamCompiler – A Simple Instruction-Based Arithmetic Compiler
This project is a lightweight command-line compiler that interprets human-readable arithmetic instructions and executes the corresponding mathematical operations.

Given an instruction like:

css
Copy
Edit
add(a,b)
The compiler will request values for a and b, then perform the operation and return the result.

💻 Supported Operations
The compiler currently supports the following operations:

Instruction	Description
add(a,b)	Adds two numbers: a + b
sub(a,b)	Subtracts b from a: a - b
mul(a,b)	Multiplies two numbers: a * b
div(a,b)	Divides a by b: a / b (b ≠ 0)
power(a,b)	Raises a to the power b: a^b
🏗️ Project Structure
plaintext
Copy
Edit
PrathamCompiler/
│
├── main.cpp                 # Entry point: reads and interprets instruction
├── instruction.txt          # Input file containing the instruction (e.g., add(a,b))
├── utils/
│   ├── instruction.cpp      # Parses the instruction from text
│   └── compute.cpp          # Executes the actual arithmetic operations
├── README.md                # Project documentation (this file)
⚙️ How to Compile and Run
Make sure you have g++ installed. Then run the following commands in your terminal:

bash
Copy
Edit
g++ main.cpp utils/instruction.cpp utils/compute.cpp -o compiler
./compiler
You will be prompted to input values for a and b. After entering them, the result will be displayed based on the operation parsed from instruction.txt.

🧪 Example Run
Suppose instruction.txt contains:

css
Copy
Edit
power(a,b)
Terminal Output:

bash
Copy
Edit
Enter value for a: 2
Enter value for b: 5
Result: 32
🛠️ Requirements
C++ compiler (tested with g++)

Terminal or command-line environment

📌 Features
Simple instruction parser

Modular design (utils/ folder for reusable logic)

Easily extendable to support more operations

Minimal dependencies – just C++

🌱 Future Improvements
Add support for more complex expressions (e.g., nested operations)

Better error handling (e.g., invalid input or division by zero)

GUI-based input interface

Support for floating-point precision
