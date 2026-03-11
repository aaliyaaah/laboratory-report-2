# Experiment 11 – Sampling and Reconstruction

---

# Overview

This experiment demonstrates the concept of **sampling and reconstruction of analog signals**, which is fundamental in digital communication systems.

Analog signals such as speech or music must first be **sampled at regular intervals** before they can be processed digitally. After sampling, the signal can be **reconstructed using filtering techniques**.

In this experiment, the **Emona Telecoms-Trainer 101** is used to sample a message signal using **natural sampling** and **sample-and-hold sampling**. The sampled signal is then passed through a **tuneable low-pass filter** to recover the original signal.

During the experiment, **two oscilloscopes were used simultaneously** to verify the signals. One oscilloscope monitored the **input message signal**, while the second oscilloscope monitored the **sampled or reconstructed output signal**.

---

# Theory

Sampling converts a **continuous analog signal** into a **discrete signal** by measuring the signal amplitude at fixed time intervals.

The sampled signal can be represented as:

Sampled Signal = Message Signal × Sampling Signal

Because the sampling signal contains a **DC component, fundamental frequency, and harmonics**, the sampled signal contains several frequency components including:

- the original message frequency  
- sum and difference frequencies  
- harmonic components  

To recover the original signal, the sampled signal is passed through a **low-pass filter** that removes higher-frequency components and allows only the **baseband message signal** to pass.

---

# Experiment Objectives

1. Observe sampling of a sinewave message signal  
2. Compare **natural sampling** and **sample-and-hold sampling**  
3. Reconstruct the sampled signal using a **low-pass filter**  
4. Investigate **aliasing distortion**

---

# Part A – Sampling a Simple Message

In this part of the experiment, a **2 kHz sinewave message signal** is sampled using an **8 kHz digital sampling signal**.

The sampling process is implemented using the **Dual Analog Switch module** of the Emona Telecoms-Trainer.

When the sampling signal switches the analog switch on and off:

- small portions of the message signal pass through  
- the output becomes a **series of pulses following the shape of the sinewave**

### Question 1

What type of sampling is this an example of?

**Answer**

Natural sampling.

### Question 2

What two features of the sampled signal confirm this?

**Answer**

- The waveform follows the **shape of the original sinewave**
- The amplitude **changes continuously during each sampling interval**

---

# Part B – Sampling Speech

In this section, the message signal is replaced with a **speech signal**.

The sampling process remains the same, but the sampled waveform now represents **variations in speech amplitude**.

Because speech signals are more complex than simple sinewaves, the sampled signal contains **multiple frequency components**.

---

# Part C – Reconstructing a Sampled Message

To recover the original signal, the sampled signal is passed through a **tuneable low-pass filter**.

Initially, the filter blocks most frequency components.

As the **cut-off frequency is increased**, the filter begins to pass the original message frequency and the waveform gradually resembles the **original sinewave message**.

---

# Part D – Aliasing

Aliasing occurs when the **sampling frequency becomes too low** relative to the message signal frequency.

In this experiment, the sampling signal is generated using the **VCO module**, which allows the sampling frequency to be gradually reduced.

As the sampling frequency decreases, the reconstructed signal begins to distort. This distortion is called **aliasing**.

### Question 3

What is the name of the distortion that appears when the sampling frequency becomes too low?

**Answer**

Aliasing distortion

### Question 4

Given the message signal is a **2 kHz sinewave**, what is the theoretical minimum sampling frequency?

**Answer**

According to the **Nyquist Sampling Theorem**, the sampling frequency must be at least **twice the message frequency**.

Minimum Sampling Frequency = **4 kHz**

### Question 5

Why is the actual minimum sampling frequency higher than the theoretical minimum?

**Answer**

In practical systems, filters are **not ideal** and cannot perfectly remove unwanted frequencies. Because of this limitation, the sampling frequency must be **slightly higher than the Nyquist rate** to avoid distortion.

---

# Observations

- Sampling converts a continuous signal into discrete samples  
- Natural sampling produces **pulse-shaped outputs**  
- Sample-and-hold produces **step-like outputs**  
- A low-pass filter reconstructs the original signal  
- Aliasing occurs when the sampling frequency is too low  
- Using **two oscilloscopes** allowed simultaneous verification of the input and output signals

---

# Conclusion

This experiment demonstrated the principles of **sampling and reconstruction** using the Emona Telecoms-Trainer 101.

The results confirmed that:

- analog signals can be sampled using switching circuits  
- sample-and-hold produces discrete amplitude levels  
- low-pass filtering reconstructs the original signal  
- the Nyquist theorem determines the minimum sampling frequency  
- sampling below the Nyquist rate causes **aliasing distortion**

---

# Pictures and Documentations

<div align="center">

<img src="https://github.com/user-attachments/assets/c8afd98b-a4fa-432a-afe7-7d1cc73406fe" width="520"><br>
<b>Figure 11.1</b>

<br><br>

<img src="https://github.com/user-attachments/assets/2f72b121-8e54-4d03-8d67-720843de9595" width="520"><br>
<b>Figure 11.2</b>

<br><br>

<img src="https://github.com/user-attachments/assets/b64484b4-58a1-49ea-b07d-4a5f33fbe3ee" width="520"><br>
<b>Figure 11.3</b>

<br><br>

<img src="https://github.com/user-attachments/assets/94ea7db1-ea6a-4900-85d2-85e530b0d411" width="520"><br>
<b>Figure 11.4</b>

<br><br>

<img src="https://github.com/user-attachments/assets/0c0cb2c5-77a8-4bf8-bb8f-c5955e18fc43" width="520"><br>
<b>Figure 11.5</b>

<br><br>

<img src="https://github.com/user-attachments/assets/ac72eaec-366e-4ad2-b99f-1500e4edb363" width="520"><br>
<b>Figure 11.6</b>

<br><br>

<img src="https://github.com/user-attachments/assets/9eb1e49c-b226-4df7-ad29-d3523557b684" width="520"><br>
<b>Figure 11.7</b>

<br><br>

<img src="https://github.com/user-attachments/assets/6dd97836-f41a-486b-86d2-f648c624fff9" width="520"><br>
<b>Figure 11.8</b>

<br><br>

<img src="https://github.com/user-attachments/assets/dda3892c-2d47-48f7-96e3-9355e380638e" width="520"><br>
<b>Figure 11.9</b>

<br><br>

<img src="https://github.com/user-attachments/assets/b251ed87-79cb-47e2-b594-c8566726daa0" width="520"><br>
<b>Figure 11.10</b>

<br><br>

<img src="https://github.com/user-attachments/assets/3a9c59c6-a3e0-4ad3-ba7b-26d4c42a0dbb" width="520"><br>
<b>Figure 11.11</b>

<br><br>

<img src="https://github.com/user-attachments/assets/de8a5a4b-2568-42fb-a13e-f780a9e28276" width="520"><br>
<b>Figure 11.12</b>

</div>
