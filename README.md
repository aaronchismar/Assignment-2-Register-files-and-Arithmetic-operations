# Assignment-2-Register-files-and-Arithmetic-operations

Register File Design
The register file consists of multiple registers, each capable of storing a 4-bit value. The design includes:
Two Read Ports: Two multiplexers are used to allow simultaneous reading of data from two different registers. The Select_read1 and Select_read2 signals determine which registers' contents are output to Read-data1 and Read-data2.


One Write Port: A decoder and control logic handle writing data to a selected register. The Select_write signal determines which register is written to, and Write_data provides the input value. A clock signal (clk) is used.

Control Logic: The ctrl_registers input makes sure that only the selected register is written when the clock signal triggers.


Register File Testing 

Writing Data to the correct register and reading off the register:
<img width="1430" alt="Screenshot 2025-03-24 at 10 13 11 PM" src="https://github.com/user-attachments/assets/6081ea87-0e5e-4e26-ba27-3ba6e0d737c4" />




ALU Implementation
The Arithmetic Logic Unit (ALU) is designed to perform basic arithmetic operations, including:
Addition: A 4-bit adder is used to sum two inputs (A and B), with a carry-in (Cin).


Subtraction: The subtract operation is handled using two NOT gates to invert B, a multiplexer to select between B and its complement, and then passing it through the adder with Cin = 1, computing A - B.


Increment/Decrement:


Incrementing is achieved by setting B = 1 and using the adder.


Decrementing is performed by setting B = -1 (1111 in two’s complement) and using the adder.


Transfer Operations: The ALU can pass A unchanged to D, effectively acting as a simple transfer function.


An overflow detection flag is included to monitor arithmetic overflows.

ALU File Testigng
Operations:

Add:
<img width="1418" alt="Screenshot 2025-03-24 at 10 29 05 PM" src="https://github.com/user-attachments/assets/5d18fe32-c6e6-413a-8cc1-95e23e46a2cf" />


Add With Carry:
<img width="1415" alt="Screenshot 2025-03-24 at 10 29 33 PM" src="https://github.com/user-attachments/assets/26abd7d1-3842-4ac0-b084-cd53c31e682d" />

Subtract With Borrow:
<img width="1413" alt="Screenshot 2025-03-24 at 10 32 51 PM" src="https://github.com/user-attachments/assets/b968ac01-5a39-440c-b796-1116e128a051" />


Subtract:
<img width="1425" alt="Screenshot 2025-03-24 at 10 33 03 PM" src="https://github.com/user-attachments/assets/b26ae0ac-021b-4ea6-8395-cb285b4e45e6" />


Transfer A:
<img width="1426" alt="Screenshot 2025-03-24 at 10 33 24 PM" src="https://github.com/user-attachments/assets/708c867b-882b-4696-be82-b54e50249ca4" />


Increment A:
<img width="1434" alt="Screenshot 2025-03-24 at 10 33 52 PM" src="https://github.com/user-attachments/assets/0aeab826-467a-4220-8b5f-944d17e695f3" />


Decrement A:
<img width="1416" alt="Screenshot 2025-03-24 at 10 34 12 PM" src="https://github.com/user-attachments/assets/8deaf0aa-0227-4f72-9b1b-25f21290c658" />


Transfer A:

<img width="1426" alt="Screenshot 2025-03-24 at 10 34 29 PM" src="https://github.com/user-attachments/assets/26434090-cba8-491a-a3aa-69ff165f6d5a" />






