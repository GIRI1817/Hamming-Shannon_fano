# NAME : GIRIDHARAN U
# REG NO : 212224060080
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
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/3c27954e-fe83-47d1-9ffc-5e658f448f58" />
<img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/ffba10e1-14af-4822-be0b-18d61063fb6a" />

# Output
<img width="489" height="344" alt="546700905-028c89ff-f642-4403-8d68-02e146538e46" src="https://github.com/user-attachments/assets/26b6e993-af9c-4891-8fcb-c9de56eec1e6" />

# Results:

The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
