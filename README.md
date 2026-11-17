# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google colab
# Program:
```
#Huffman and Shannon-Fano coding
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
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy
red =  round(1 - eff,3)
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
<img width="1204" height="1600" alt="WhatsApp Image 2026-10-30 at 10 50 03 AM" src="https://github.com/user-attachments/assets/50fffeab-62d9-49d9-b590-70517a6b8720" />

<img width="1178" height="1600" alt="WhatsApp Image 2026-10-30 at 10 50 02 AM" src="https://github.com/user-attachments/assets/0051473e-f609-4290-9eac-8b9d8a7ec094" />



# Output

<img width="497" height="360" alt="image" src="https://github.com/user-attachments/assets/b1ce58a0-5183-4c41-bd4c-fac2ec84c5b9" />

# Results:
The Huffman and Shannon-Fano of the given statistics {0.4, 0.19, 0.16, 0.15, 0.15} using python are verified.
