# Fitting Poisson  distribution
# Aim : 

To fit poisson distribution for the arrival of objects per minute from the feeder

# Software required :  

Python and Visual component tool

# Theory:

The Poisson distribution is the discrete probability distribution of the number of events occurring in a given time period, given the average number of times the event occurs over that time period.

![image](https://user-images.githubusercontent.com/104613195/166248326-fd042076-8b0b-40c4-8b11-1d8e8fcb74db.png)

 Conditions for Poisson Distribution:

1. An event can occur any number of times during a time period.
2. Events occur independently. I
3. The rate of occurrence is constant.
4. The probability of an event occurring is proportional to the length of the time period. 
 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/166251988-d0c53205-6080-4f7b-ae4c-398178586637.png)

# Experiment :

![image](https://user-images.githubusercontent.com/103921593/230282876-f4a5afbf-cac1-4648-a1b0-c78840638a8e.png)

# Program :
```
import numpy as np
n = int(input("Enter the value of n : "))
print("Value of n =", n)
InputVal = {}
for i in range(1, n+1):
val = int(input(f"Enter the value no {i} : "))
try:
InputVal[val] += 1
except:
InputVal[val] = 1
print(f"{i} Values Collected Successfully")
mean = 0
for key, val in InputVal.items():
mean += key*(val/n)
print(f"Mean = {mean:.3f}")
ex2 = 0
for key, val in InputVal.items():
ex2 += ((key**2) * val/n)
var = ex2 - mean**2
print(f"Variance : {var:.3f}")
from math import sqrt
sdtDeviation = sqrt(var)
print(f"Standard Deviation = {sdtDeviation:.3f}")
```

 

# Output :
<img width="385" height="262" alt="{34B2F455-6383-4894-A5B7-7C0D7C60981C}" src="https://github.com/user-attachments/assets/7513a2ef-8094-4282-bf2a-61632a5e97c2" />




# Results

The Poisson distribution is fitted for the objects arrived from feeder per minute and the data is tested using Chi-square test. 
 
