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
|          2000           |        A4                |
|          2001           |        18                |
|          2002           |        57                |
|          2003           |        1B                |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          2004           |        FB                |
|          2005           |        33                |
|          2006           |        00                |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 12 54 55_5dd49785](https://github.com/user-attachments/assets/99c8b09a-599a-4a8e-8c12-f6cd69bb798c)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="431" alt="add_indirect" src="https://github.com/user-attachments/assets/189dbb5a-3028-4a5b-9a22-65f15bf36ad6" />


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
|          2000           |        84                |
|          2001           |        14                |
|          2002           |        57                |
|          2003           |        1B                |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          2004           |        FF                |
|          2005           |        03                |
|          2006           |        00                |
#### Manual Calculations

![WhatsApp Image 2025-09-22 at 12 54 56_0ae69f30](https://github.com/user-attachments/assets/509e9f7e-29a6-462a-b912-575a261c6ab2)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="436" alt="sub_indirect" src="https://github.com/user-attachments/assets/4e7c0808-555b-43b6-8888-a282a4f101c1" />


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
|          2000           |        02                |
|          2001           |        00                |
|          2002           |        03                |
|          2003           |        00                |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          2004           |        06                |
|          2005           |        00                |
|          2006           |        00                |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 12 54 56_3a1c7bbc](https://github.com/user-attachments/assets/fc61f071-2637-4012-a6bc-1c5170b7f0e2)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="629" height="426" alt="mul_indirect" src="https://github.com/user-attachments/assets/6274d785-df04-4a89-b9f5-275fe4b74162" />


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
|          2000           |        69                |
|          2001           |        24                |
|          2002           |        34                |
|          2003           |        12                |


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          2004           |        02                |
|          2005           |        00                |
|          2006           |        01                |

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 12 54 55_55ca5c1a](https://github.com/user-attachments/assets/658c0103-d43c-46b2-b885-3147c6a5376c)


---
## OUTPUT FROM MASM SOFTWARE

<img width="621" height="425" alt="div_indirect" src="https://github.com/user-attachments/assets/ffda9843-e067-4e56-9f68-2fecbaeacd64" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

