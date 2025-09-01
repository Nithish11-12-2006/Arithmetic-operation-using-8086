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
MOV SI,1200H
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
| ----1200 : 12---------- |   1204 : 24------------- |
| ----1201 : 34---------- |   1205 : 68------------- |
| ----1202 : 12---------- |   1206 : 00------------- |
| ----1203 : 34---------- |   1207 : C4------------- |

#### Manual Calculations

![nithish1(addi)](https://github.com/user-attachments/assets/38984e18-d129-44a3-89c0-f3fd1cbbb03b)

---
## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="nithish1" src="https://github.com/user-attachments/assets/5c52a89f-f242-425b-94a3-26a5c88ad1f7" />

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
MOV SI,1200H
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
| ----1200 : 12---------- |   1204 : 00------------- |
| ----1201 : 34---------- |   1205 : 00------------- |
| ----1202 : 12---------- |   1206 : 00------------- |
| ----1203 : 34---------- |   1207 : C4------------- |

#### Manual Calculations

![nithish2(subt)](https://github.com/user-attachments/assets/6ba10f6d-575b-4a07-8261-2d29943873d6)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="nithish2" src="https://github.com/user-attachments/assets/862f58cb-c1bd-4af9-9666-2600cdc65c1b" />


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
MOV SI,1200H
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
| ----1200 : 12---------- |   1204 : 44------------- |
| ----1201 : 34---------- |   1205 : 51------------- |
| ----1202 : 12---------- |   1206 : 97------------- |
| ----1203 : 34---------- |   1207 : 0A------------- |

#### Manual Calculations

![nithish3(multi)](https://github.com/user-attachments/assets/09112770-5ea8-4c58-8b26-4cea78a8a128)



---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="nithish3" src="https://github.com/user-attachments/assets/0753e49e-5b2a-4fb4-97e6-e8e17f3e50b7" />


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
MOV SI,1200H
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
| ----1200 : 12---------- |   1204 : 01------------- |
| ----1201 : 34---------- |   1205 : 00------------- |
| ----1202 : 12---------- |   1206 : 00------------- |
| ----1203 : 34---------- |   1207 : 00------------- |

#### Manual Calculations

![nithish4(divi)](https://github.com/user-attachments/assets/d759603a-dce0-4b13-ba54-994ee2fd587e)

---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="nithish4" src="https://github.com/user-attachments/assets/60de644e-42b5-4da8-8b4d-a84ac9b8720e" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
