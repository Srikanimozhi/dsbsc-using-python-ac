# dsbsc-using-python-ac

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics.

EQUIPMENTS REQUIRED

• Computer with i3 Processor • CO LAB.

Note: Keep all the switch faults in off position

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE
• Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

image
Program

import numpy as np
import matplotlib.pyplot as plt
Am =5    
Ac =10   
fm = 777   
fc = 7770    
fs = 77700   
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()

Output:
<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/037a04cb-22e1-471a-b2d0-7d92c4a21f3f" />

calculation:
![WhatsApp Image 2025-10-23 at 23 22 12_8ab44c2d](https://github.com/user-attachments/assets/31a80bc9-a9fd-497d-93b1-674b9e9b4884)


Result:


Thus the DSB-SC-AM Modulation and Demodulation using python is generated.
