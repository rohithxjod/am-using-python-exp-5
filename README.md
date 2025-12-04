# AM-using-python


## Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy andq Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
```
import numpy as np
import matplotlib.pyplot as plt
Am=5.3
fm=457
Ac=10.6
fc=4570
fs=45700
t=np.arange(0,2/fm,1/fs)
m = np.cos(2 * np.pi * fm * t)
c=np.cos(2*np.pi*fc*t)
s = (Ac+Am*np.cos(2*np.pi*fm*t))*np.cos(2*np.pi*fc*t)

plt.subplot(3,1,1)
plt.plot(t, m)

plt.subplot(3,1,2)
plt.plot(t,c)

plt.subplot(3,1,3)
plt.plot(t,s)



```

## Output Waveform
<img width="677" height="506" alt="image" src="https://github.com/user-attachments/assets/c5a31828-7e58-4595-8bf4-745bd12d52e3" />

## Tabular Column

![5 ac](https://github.com/user-attachments/assets/61c8568f-f659-48a8-be25-655f225a919e)





## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
