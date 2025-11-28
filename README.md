# DSBSC-using-Python

## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries. 

## EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer

## Algorithm:

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program

````
import numpy as np
import matplotlib.pyplot as plt

Am=7.6
fm=687
fc=6870
fs=68700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
Ac=15.2
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*np.pi*fc*t)
s2=(Ac-m)*np.cos(2*np.pi*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
plt.show()
````


## Output Graph

<img width="845" height="617" alt="image" src="https://github.com/user-attachments/assets/ce1030e1-0395-4ac0-b906-a6f97a3e598c" />





## Tablular Column

![WhatsApp Image 2025-11-28 at 22 03 18_10a8a656](https://github.com/user-attachments/assets/8be48d7b-ece4-4543-b1be-312a1b14c81b)


## Result

Thus the DSB-SC-AM Modulation is generated using python.
