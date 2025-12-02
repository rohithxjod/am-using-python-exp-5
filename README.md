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
Am=4.5
fm=374
Ac=9.0
fc=3740
fs=37400
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

<img width="693" height="516" alt="image" src="https://github.com/user-attachments/assets/957d74ad-929d-4bd9-94c3-770b8fa9efb6" />





## Tabular Column

![WhatsApp Image 2025-11-29 at 08 24 28_8f31838d](https://github.com/user-attachments/assets/ac9eeb59-3d4a-483e-8ebd-941c3508b811)




## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
