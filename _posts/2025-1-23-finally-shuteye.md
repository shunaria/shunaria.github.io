---
title : making a half triangle with number using 8086 compiler
date : 2025-1-23 00:00:00 +0800
categories : [8086 compiler]
tags : [one of my code]
image :
    path :  assets/images/overwork.jpg
---

this is code to make a half triangle that uses assembely language which is run on 8086 compiler 
```
start:
mov ah, 0x13
mov al, 0x31
mov cx, 1
mov bh, 1
a:
mov bl, 0
b:
mov byte ds[bp], al
inc bl
inc bp
cmp bl, bh
jne b
c:
inc bh
inc cx
inc al
mov bp, 0
int 0x10
cmp bh,5
je end
jmp a
end:
hlt
```
the use of the code above is that it make use of the "mov byte ds[bp], al" to make it so that in the memory there is 1 , 31(hex) save from the al, which is later gonna be increase to 34(hex) which will later be conferted to 1-4 in decimal.
which will later make an output 
```
1
22
333
4444
```
this is a more deatailed information for each line of the code 

start: (to tell the compiler from where the code start) 

mov ah, 0x13(to set “ah” to hex 13)  

mov al, 0x31(to set “al” to hex 31) 

mov cx, 1(to set “cx” to int 1) 

mov bh, 1(to set “bh” to int 1) 

a: (as a label if theres a jump fuction later use)  

mov bl, 0 (set “bl” to int 0) 

b: (as a label if theres a jump fuction later use) 

mov byte ds[bp], al (to set the data in memory to follow “al”) 

inc bl (increase the number of “bl” by 1 ) 

inc bp (increase the number of “bp” by 1 ) 

cmp bl, bh (compare “bl” with “bh”)  

jne b (jump if not equal back to the label b ) 

c: (as a label if theres a jump fuction later use) 

inc bh (increase the number of “bh” by 1)  

inc cx (increase the number of “cx” by 1)  

inc al (increase the number of “al” by 1)  

mov bp, 0 (to set “bp” to int 0) 

int 0x10 (this is use to print whats in memory ) 

cmp bh, 5 (compare “bh” with 5) 

je end (jump if equal to the label end) 

jmp a (jump to a) 

end: (as a label if theres a jump fuction later use) 

hlt(to stop the compiler) 