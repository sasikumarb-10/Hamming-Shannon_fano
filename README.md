# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
eff = hs / L
eff = round(eff,3)
red =  round(1 - eff,3) 
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print()
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff*100} %")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

![WhatsApp Image 2026-02-06 at 14 03 45](https://github.com/user-attachments/assets/b9def89a-bcc0-4d73-a081-c537d2ef3514)
![WhatsApp Image 2026-02-06 at 14 03 45 (1)](https://github.com/user-attachments/assets/d11ae35a-1605-4c28-9ac6-63030b1bb657)

# Output
```
Enter the number of Samples : 7
Enter the probability of sample values 1: 0.25
Enter the probability of sample values 2: 0.25
Enter the probability of sample values 3: .125
Enter the probability of sample values 4: 0.125
Enter the probability of sample values 5: 0.125
Enter the probability of sample values 6: 0.0625
Enter the probability of sample values 7: 0.0625
Enter the length of the sample values 1: 2
Enter the length of the sample values 2: 2
Enter the length of the sample values 3: 3
Enter the length of the sample values 4: 3
Enter the length of the sample values 5: 3
Enter the length of the sample values 6: 4
Enter the length of the sample values 7: 4
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 1.0
Redudancy is : 0.0
Variance is : 0.484
```
# Results:

The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
