# Experiment 12 – PCM Encoding

## Overview
This experiment demonstrates Pulse Code Modulation (PCM), a method used to convert analog signals into digital form. The PCM Encoder module samples an analog voltage, quantizes the sample to the nearest level, and produces an 8-bit binary output representing that level.

The experiment investigates:

- PCM encoding using a fixed DC input
- PCM encoding using a variable DC voltage
- Quantisation effects
- PCM encoding of continuously changing signals

---

## Theory
Pulse Code Modulation converts an analog signal into digital form through the following steps:

1. Sampling – measuring the signal at regular intervals.
2. Quantisation – comparing the sample to reference voltage levels.
3. Encoding – assigning a binary number representing the closest quantisation level.
4. Serial transmission – sending the binary number one bit at a time.

The PCM Encoder module converts voltages between approximately −2 V and +2 V into an 8-bit binary number. Since 8 bits are used, the system has 256 possible quantisation levels.

Because the sampled voltage may not match a quantisation level exactly, the difference between the real value and the quantised value is called **quantisation error**.

---

# Part A – PCM Encoding Using a Static DC Voltage

In this section the PCM Encoder converts a fixed DC voltage into a binary number.

### Question 1  
Indicate on your drawing the start and end of the frame.

**Answer:**  
The frame begins at the Frame Synchronisation (FS) pulse and ends before the next FS pulse.

### Question 2  
Indicate on your drawing the start and end of each bit.

**Answer:**  
Each bit begins and ends according to the clock signal period.

### Question 3  
Indicate which bit is bit-0 and which is bit-7.

**Answer:**  
Bit-7 is the most significant bit transmitted first, and bit-0 is the least significant bit transmitted last.

### Question 4  
What is the binary number that the PCM Encoder module is outputting?

**Answer:**  
The output binary number corresponds to the quantisation level closest to the input DC voltage.

### Question 5  
Why does the code change even though the input voltage is steady?

**Answer:**  
Small noise variations and quantisation boundaries can cause the sampled voltage to move between adjacent quantisation levels.

### Question 6  
Why does the PCM Encoder module output this code for 0 V DC and not 00000000?

**Answer:**  
Because 0 V lies near the middle of the quantisation range, the encoder outputs the code corresponding to the middle quantisation level instead of the lowest code.

---

# Part B – PCM Encoding of a Variable DC Voltage

In this section the DC voltage is varied to observe how the binary output changes.

### Question 7  
What happens to the Variable DCV module’s output?

**Answer:**  
The output voltage gradually increases as the control is turned clockwise.

### Question 8  
In what way does the binary number that the PCM Encoder module outputs change?

**Answer:**  
The binary number increases step by step as the input voltage increases.

### Question 9  
Explain why you may not be able to obtain the output 11111111.

**Answer:**  
The Variable DC module may not reach the maximum voltage required for the PCM Encoder input range, preventing the highest code from appearing.

### Question 10  
Devise a method to obtain a variable DC voltage that reaches the limits of the encoder input.

**Answer:**  
A signal conditioning or amplification stage can be used so the variable DC voltage spans the entire encoder input range.

### Question 11  
What happens to the binary number when the negative input voltage increases?

**Answer:**  
The binary output decreases as the input voltage becomes more negative.

### Question 12  
What is the maximum allowable peak-to-peak amplitude for an AC signal on the PCM Encoder input?

**Answer:**  
Approximately 4 V peak-to-peak, corresponding to the −2 V to +2 V input range.

---

# Part C – Quantisation

### Question 13  
What is the name for the difference between a sampled voltage and its closest quantisation level?

**Answer:**  
Quantisation error.

### Question 14  
Calculate the difference between quantisation levels.

**Answer:**  
Quantisation step size ≈ 4 V / 256 ≈ 0.0156 V.

### Question 15  
To reduce quantisation error it is better to have:

**Answer:**  
More quantisation levels between ±2.5 V.

---

# Part D – PCM Encoding of Continuously Changing Voltages

In this part the PCM Encoder converts a continuously varying signal into digital form.

### Question 16  
Why does the PCM DATA change continuously?

**Answer:**  
Because the input signal is continuously changing, each sampled value corresponds to a different quantisation level, producing continuously changing binary output.

---

# Conclusion
This experiment demonstrated how Pulse Code Modulation converts analog voltages into digital codes. The PCM Encoder samples the signal, quantizes it to the nearest level, and outputs the corresponding binary value. The experiment also showed how quantisation error occurs and how increasing the number of quantisation levels reduces this error.

---

# Pictures and Documentations
<p align="center">
<img src="https://github.com/user-attachments/assets/b56586ab-2423-4a79-a0c9-e413bbd014f1" width="700">
</p>
<p align="center">
<b>Figure 12.1</b>
</p>

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/388e74cd-0760-4799-be6f-7bc56783bcbe" width="700">
</p>
<p align="center">
<b>Figure 12.2</b>
</p>

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/eb022647-7cbf-4e0e-a49a-e0645c4603af" width="700">
</p>
<p align="center">
<b>Figure 12.3</b>
</p>

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/5331b72b-d7ba-49f4-bb18-f1facbeac336" width="700">
</p>
<p align="center">
<b>Figure 12.4</b>
</p>

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/d177a177-e3ba-4708-bc89-72e1a0f59ca9" width="700">
</p>
<p align="center">
<b>Figure 12.5</b>
</p>

<br>

<p align="center">
<img src="https://github.com/user-attachments/assets/060513d5-491c-44ed-b05f-ec732a5f5200" width="700">
</p>
<p align="center">
<b>Figure 12.6</b>
</p>
