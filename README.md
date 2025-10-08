# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-10 at 10 35 32_c136f9c0](https://github.com/user-attachments/assets/ce61f905-bd72-44ce-b50d-d6afb60eb86e)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-10 at 10 36 10_ef94d368](https://github.com/user-attachments/assets/b97c4b10-5eab-4fad-bd1f-d94d3988fb76)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
![WhatsApp Image 2025-09-10 at 10 36 08_e1be1e05](https://github.com/user-attachments/assets/a5db329b-8bd2-44a2-8881-2b57801fd5b6)



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|    1200=12	           |        1204=00           |
|    1201=34	           |        1205=00           |
|    1202=12	           |                          |
|    1203=34	           |                          |

#### Manual Calculations

(Add your calcula![WhatsApp Image 2025-09-10 at 10 35 30_3f316649](https://github.com/user-attachments/assets/ef274c66-48c6-4536-a0be-efaedffbf43d)
tion here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-10 at 10 36 10_10e57e39](https://github.com/user-attachments/assets/3d417d30-8c3c-43ae-a2ed-97568d172121)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          1200=12	     |         1204=44          |
|          1201=34	     |         1205=51          |
|          1202=12	     |         1206=97          |
|          1204=34	     |         1207=0           |                    

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-10 at 10 35 31_c9a89528](https://github.com/user-attachments/assets/ee2f59dd-9ce4-4c51-965a-f6c8866070a4)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-10 at 10 36 09_15254bc5](https://github.com/user-attachments/assets/7e5d1452-ddb0-450c-a580-dcf774e1f4c6)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          1200=12	     |        1204=01           |
|          1201=34	     |        1205=00           |
|          1202=12	     |                          |
|          1203=34        |                          |

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-10 at 10 35 32_cd4ea95d](https://github.com/user-attachments/assets/74ce9b17-b564-4dcc-8f91-4818204657e2)

---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-10 at 10 36 09_a27d2f8a](https://github.com/user-attachments/assets/7bf8a700-1a80-4772-acfa-b1d82bf40f10)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
