# Experiment 10 – FM Demodulation

---

# Overview

This experiment demonstrates the **demodulation of a Frequency Modulated (FM) signal**. The objective is to recover the original message signal from an FM waveform using a **Zero-Crossing Detector (ZCD)** method.

An FM signal is first generated using a **Voltage Controlled Oscillator (VCO)**. The signal is then processed through a **comparator**, a **zero-crossing detector**, and a **baseband low-pass filter** to recover the original message signal.

This experiment demonstrates:

- FM signal demodulation  
- Operation of a **Zero-Crossing Detector (ZCD)**  
- Recovery of the original message signal using filtering  

---

# Theory

## FM Demodulation

Frequency demodulation is the process of **recovering the original message signal from a frequency-modulated carrier**.

In this experiment, demodulation is performed using a **Zero-Crossing Detector (ZCD)**. This method converts frequency variations into **changes in pulse spacing and duty cycle**, which can then be filtered to obtain the original message signal.

The demodulation process involves:

1. Comparator  
2. Zero-Crossing Detector (ZCD)  
3. Baseband Low-Pass Filter  

---

# Zero-Crossing Detector Principle

The FM signal is first clipped by a **comparator**, converting the sinusoidal waveform into a squarewave. This squarewave acts as a trigger signal for the **zero-crossing detector**.

The ZCD produces a pulse every time the input signal crosses **zero volts**. Because the FM signal's frequency changes according to the message signal, the **spacing between pulses also changes**.

The pulse width remains constant while the spacing between pulses varies. This means that the **duty cycle of the pulse train changes according to the input frequency**.

A **low-pass filter** then extracts the varying DC component of the pulse train, which reconstructs the **original message signal**.

---

# Conceptual Block Diagram

<p align="center">
<img src="https://github.com/user-attachments/assets/f776712a-1bb6-4ca1-a921-b3cedb065c5d" width="700">
</p>

<p align="center">
<b>Figure 10.1</b> – FM Demodulation Block Diagram
</p>

---

# Experimental Setup

<p align="center">
<img src="https://github.com/user-attachments/assets/fef32a1a-fc0f-4c45-b926-8611289b8a61" width="700">
</p>

<p align="center">
<b>Figure 10.2</b> – FM Demodulator Setup Using the Emona Telecoms Trainer
</p>

---

# Complete FM Modulator and Demodulator System

<p align="center">
<img src="https://github.com/user-attachments/assets/7e69e263-ba95-407e-8875-c18cee9f0994" width="700">
</p>

<p align="center">
<b>Figure 10.3</b> – Complete FM Modulation and Demodulation System
</p>

---

# Oscilloscope Observations

### FM Signal

<p align="center">
<img src="https://github.com/user-attachments/assets/5ba86d43-7a3f-4e6f-9fca-a34b25647a37" width="700">
</p>

<p align="center">
<b>Figure 10.4</b> – FM Signal Observed on the Oscilloscope
</p>

---

### Comparator Output

<p align="center">
<img src="https://github.com/user-attachments/assets/2843d47f-70c7-4f11-af5f-d8407b61bce4" width="700">
</p>

<p align="center">
<b>Figure 10.5</b> – Comparator Output Squarewave
</p>

---

### Zero Crossing Detector Output

<p align="center">
<img src="https://github.com/user-attachments/assets/f8a92c35-413a-4589-a8a8-5de0726424b2" width="700">
</p>

<p align="center">
<b>Figure 10.6</b> – ZCD Pulse Train Output
</p>

---

### Demodulated Output

<p align="center">
<img src="https://github.com/user-attachments/assets/bc418f53-694e-4c09-89d1-4dd7dec366db" width="700">
</p>

<p align="center">
<b>Figure 10.7</b> – Demodulated Message Signal After Baseband LPF
</p>

---

### Final Output Signal

<p align="center">
<img src="https://github.com/user-attachments/assets/87b831cc-c378-4389-885a-91158fa2982e" width="700">
</p>

<p align="center">
<b>Figure 10.8</b> – Final Recovered Signal
</p>

---

# Questions

### Question 1  
**Why is the FM signal no longer a sinewave?**

The FM signal is no longer a sinewave because it passes through a **comparator**, which clips the waveform and converts it into a **squarewave**.

---

### Question 2  
**What type of waveform does the comparator output?**

The comparator outputs a **squarewave signal**.

---

### Question 3  
**What does this tell us about the DC component of the comparator's output?**

The DC component depends on the **duty cycle of the pulse train** produced after the ZCD stage.

---

### Question 4  
**What type of waveform does the ZCD output?**

The ZCD produces a **rectangular pulse train**.

---

### Question 5  
**As the FM signal changes frequency so does the ZCD output. What aspect of the signal changes?**

**Only the spacing between pulses changes**.

---

### Question 6  
**What does this tell us about the DC component of the signal?**

The DC component varies according to the **duty cycle of the pulse train**, which corresponds to the original message signal.

---

### Question 7  
**If the original message is a sinewave instead of a variable DC voltage, what would appear at the Baseband LPF output?**

The Baseband LPF would output a **sinewave similar to the original message signal**.

---

### Question 8  
**What does the FM demodulator output tell you about the ZCD duty cycle?**

The output shows that the **duty cycle of the ZCD pulses varies according to the message signal**, allowing the original signal to be recovered after filtering.

---

# Conclusion

This experiment demonstrated how a **Zero-Crossing Detector can demodulate an FM signal**. The comparator converts the FM signal into a squarewave, the ZCD converts frequency variations into pulse spacing variations, and the low-pass filter extracts the DC component corresponding to the original message signal.

The recovered output confirms the effectiveness of the **FM demodulation process using the ZCD method**.
