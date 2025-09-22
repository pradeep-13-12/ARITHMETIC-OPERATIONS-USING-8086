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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 32 38_9d6d7ce1](https://github.com/user-attachments/assets/533802a2-3ce7-4046-aaf1-784b7ade2074)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 19 02_e089825c](https://github.com/user-attachments/assets/7e0fbba4-6100-43c6-a5c6-9e3785b33e0d)
![WhatsApp Image 2025-09-22 at 08 23 05_a5bf5449](https://github.com/user-attachments/assets/d68f6dc4-b2e2-483a-946d-8ab14abed43e)

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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations


![WhatsApp Image 2025-09-22 at 08 36 44_69bbc167](https://github.com/user-attachments/assets/8a931e16-5e11-443c-ba1a-5a51baffe43c)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 23 05_971dc4fa](https://github.com/user-attachments/assets/7cb4f130-e091-4de7-8d65-1ee006d23cbb)
<img width="645" height="445" alt="Screenshot 2025-08-18 113509" src="https://github.com/user-attachments/assets/0e1f9828-648b-40b4-ab29-dee3cf1610e9" />

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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations

![WhatsApp Image 2025-09-22 at 08 43 11_36f250bf](https://github.com/user-attachments/assets/015ead3a-a5be-4c66-9eb8-6925141b7047)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-22 at 08 23 05_1c5e6c5a](https://github.com/user-attachments/assets/eb7a550f-930a-4533-8792-e846670701a1)
<img width="638" height="445" alt="Screenshot 2025-08-18 112949" src="https://github.com/user-attachments/assets/ed9bf19e-01c4-46c2-a209-cab3cb9cfc5a" />

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
|     1200:12 24:1204     |                          |
      1201:34                    68:1205
      1202:12                    00:1206
      1203:34                    c4:1207

#### Manual Calculations


![WhatsApp Image 2025-09-22 at 08 47 03_148ecfc2](https://github.com/user-attachments/assets/da5818fb-0439-4502-8e93-9ea418fdb18f)

---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-22 at 08 23 05_0894f270](https://github.com/user-attachments/assets/1d80e010-3ff8-44f3-8e5b-83086699d311)


<img width="638" height="434" alt="Screenshot 2025-08-18 112739" src="https://github.com/user-attachments/assets/a4ca021e-195f-4b28-ba51-5551fe3ee7a7" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

