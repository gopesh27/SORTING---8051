
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H 
MOV R6,#04
LOOP: MOV A,@R0 
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JNC DOWN 
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```

**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:

<img width="955" height="170" alt="image" src="https://github.com/user-attachments/assets/254f0052-e773-48d9-80c0-7b852128796d" />

After execution: D:0x40H:

<img width="955" height="170" alt="image" src="https://github.com/user-attachments/assets/307abe82-9f36-4b89-a9e2-d48e956ac6b2" />

**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H
MOV R6,#04
LOOP: MOV A,@R0
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT
SJMP DOWN 
NEXT:JC DOWN
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:** D:0x40H:

<img width="955" height="170" alt="image" src="https://github.com/user-attachments/assets/bf270e8a-e8f5-44b7-b5d2-56ac04c272be" />

After execution: D:0x40H:

<img width="955" height="170" alt="image" src="https://github.com/user-attachments/assets/e9cbb54e-995b-4b03-8e00-9182f3cea50d" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

