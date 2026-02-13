# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
CMC
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP: CMP M
JNC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```
## Output:
<img width="1909" height="1035" alt="Screenshot 2026-02-13 161421" src="https://github.com/user-attachments/assets/a7935732-f727-45ef-ad67-dfd4117cabe9" />
<img width="1919" height="1032" alt="Screenshot 2026-02-13 161433" src="https://github.com/user-attachments/assets/1cc19bb3-d4be-4c32-b6b0-f9b3c1c14770" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
CMC
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP: CMP M
JC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 4301H
HLT
```
## Output:
<img width="1616" height="825" alt="Screenshot 2026-02-13 204745" src="https://github.com/user-attachments/assets/6de9d6ca-f1af-4334-8c15-f16ed1321488" />
<img width="292" height="365" alt="image" src="https://github.com/user-attachments/assets/e69b1102-f031-448b-9ac5-990a0af7cfde" />

## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
