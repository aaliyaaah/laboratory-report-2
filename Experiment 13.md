# Experiment 13 – PCM Decoding

---

## Overview

This experiment demonstrates the **decoding process of Pulse Code Modulation (PCM)**.  
PCM is used to convert analog signals into digital data for transmission. In this experiment the digital PCM signal is decoded back into an analog signal.

The experiment investigates:

- How PCM data frames are interpreted
- How binary data is converted into an analog voltage
- The effect of quantization during decoding
- Reconstruction of the original signal using a **low-pass filter**

---

## Theory

Pulse Code Modulation converts analog signals into digital form through **sampling, quantization, and encoding**.

During decoding the following steps occur:

1. Detect the **start of each frame** in the PCM data stream.
2. Extract the **binary number** representing the sampled voltage.
3. Convert the binary number into a **corresponding analog voltage**.
4. Hold the voltage until the next frame arrives.
5. Pass the signal through a **low-pass filter** to reconstruct the message.

The PCM decoder must operate using the **same clock frequency as the encoder**. If the clocks differ, some bits may be missed or interpreted incorrectly.

Frame synchronization is also required so that the decoder knows **where each binary word begins**.

---

# Part A – Setting up the PCM Encoder

To perform PCM decoding, PCM data must first be generated using the **PCM Encoder module**.

The encoder converts the analog input voltage into binary PCM data using a **100 kHz clock signal** from the Master Signals module.

The oscilloscope is used to observe:

- Frame synchronization signal (FS)
- PCM DATA output

These signals allow verification that the encoder is operating correctly.

### Figures

<p align="center">
<img src="https://github.com/user-attachments/assets/44f57c8e-d8d5-4b1e-bf78-2b10a91bf06f" width="700">
</p>

<p align="center"><b>Figure 13.1 – PCM encoder block diagram.</b></p>

<p align="center">
<img src="https://github.com/user-attachments/assets/4afda74d-c310-4c73-b194-eb5d1e849722" width="700">
</p>

<p align="center"><b>Figure 13.2 – Actual PCM encoder setup used in the experiment.</b></p>

---

# Part B – Decoding the PCM Data

The PCM Decoder module receives the PCM DATA output from the encoder.

The decoder also requires:

- Clock signal
- Frame synchronization signal

These are obtained directly from the encoder so the decoder remains synchronized.

The decoder interprets each **8-bit PCM word** and converts it into a corresponding analog voltage.

### Figures

<p align="center">
<img src="https://github.com/user-attachments/assets/f3409ba7-292d-43b1-8dc3-69d3133f686d" width="700">
</p>

<p align="center"><b>Figure 13.3 – PCM encoding and decoding system block diagram.</b></p>

<p align="center">
<img src="https://github.com/user-attachments/assets/8ba6a74b-ac8f-4f72-bbf8-c084c4118947" width="700">
</p>

<p align="center"><b>Figure 13.4 – Initial decoding setup showing PCM encoder and decoder connections.</b></p>

<p align="center">
<img src="https://github.com/user-attachments/assets/ccf5ea99-40ea-41a3-9c50-3896cf429463" width="700">
</p>

<p align="center"><b>Figure 13.5 – Oscilloscope observation of the decoded PCM signal.</b></p>

---

### Question 1

**What does the PCM Decoder’s “stepped” output tell you about the type of signal that it is?**

**Answer**

The stepped output indicates that the signal is **quantized and sampled**, not continuous.  
Each step represents a discrete voltage level corresponding to a quantization level from the PCM encoding process.

---

# Part C – Encoding and Decoding Speech

In this section a **speech signal** is used as the message signal instead of a simple sine wave.

The signal is:

1. Encoded by the PCM encoder  
2. Transmitted as PCM DATA  
3. Decoded by the PCM decoder  
4. Compared to the original signal

A buffer module allows the signal to be heard through headphones.

### Figures

<p align="center">
<img src="https://github.com/user-attachments/assets/68ca6a07-0f5d-4e4d-b5f7-c58d726d4d68" width="700">
</p>

<p align="center"><b>Figure 13.6 – PCM system output without speech input.</b></p>

---

### Question 2

**What must be done to the PCM Decoder module’s output to reconstruct the message properly?**

**Answer**

The decoder output must be passed through a **low-pass reconstruction filter**.  
This removes the high-frequency components caused by sampling and converts the stepped PAM signal into a smooth waveform.

---

# Part D – Recovering the Message

To fully reconstruct the original message signal, the decoder output is passed through a **tunable low-pass filter module**.

The filter removes high-frequency sampling components and produces a waveform that closely resembles the original message signal.

### Figures

<p align="center">
<img src="https://github.com/user-attachments/assets/afbf368c-27fe-45aa-868d-fff209288b72" width="700">
</p>

<p align="center"><b>Figure 13.7 – Reconstruction block diagram using a low-pass filter.</b></p>

<p align="center">
<img src="https://github.com/user-attachments/assets/b698146d-5b8d-47d1-b3e9-3e332d0ec87c" width="700">
</p>

<p align="center"><b>Figure 13.8 – Final experimental setup with tunable low-pass filter.</b></p>

---

### Question 3

**Even though the two signals look and sound the same, why isn’t the reconstructed message a perfect copy of the original message?**

**Answer**

The reconstructed signal is not perfect because of **quantization error and sampling effects**.  
During PCM encoding the analog signal is approximated to the nearest quantization level. When the signal is decoded these approximations remain, producing small errors in the reconstructed waveform.

---

# Conclusion

This experiment demonstrated the **decoding process of Pulse Code Modulation**.

The PCM decoder successfully converted the digital PCM data stream into a PAM signal representing the original message. By applying a **low-pass reconstruction filter**, the message signal was recovered and closely resembled the original waveform.

However, due to **quantization and sampling limitations**, the reconstructed signal is not an exact replica of the original signal.
