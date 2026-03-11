# Experiment 14 – Bandwidth Limiting and Restoring Digital Signals

---

## Overview

This experiment demonstrates how **bandwidth limitations affect digital communication systems** and how distorted signals can be restored.

In practical communication channels, the transmission medium has a **limited bandwidth**. When a digital signal passes through a channel with insufficient bandwidth, the signal becomes distorted because some of its higher frequency components are attenuated.

This experiment investigates:

- The effect of **bandwidth limiting on PCM decoding**
- How bandwidth affects the **shape of digital signals**
- Use of a **low-pass filter to model a communication channel**
- Restoration of distorted digital signals using a **comparator**
- Observation of digital signal quality using **eye diagrams**

---

## Theory

Digital signals are composed of many sinusoidal components known as **harmonics**. These harmonics combine to produce the sharp transitions present in square waves.

When a communication channel has limited bandwidth:

- Higher frequency harmonics are **attenuated**
- Digital edges become **rounded**
- Logic levels become **uncertain**
- Receivers may **misinterpret the data**

These effects can cause decoding errors in systems such as **PCM communication systems**.

To study these effects, the experiment uses a **Tunable Low-Pass Filter** to simulate a bandwidth-limited communication channel.

---

# Part A – Effects of Bandwidth Limiting on PCM Decoding

In this section a PCM communication system is constructed using the **Variable DCV module** as the message source.  
The signal is encoded by the **PCM Encoder module**, transmitted through the channel, and decoded by the **PCM Decoder module**.

The oscilloscope is used to observe the signals in the system.

<div align="center">

<img src="https://github.com/user-attachments/assets/446a57d8-08cf-4575-87e5-c57176fca0a8" width="700"><br>
<b>Figure 14.1.</b> Block diagram of the PCM communication system.

<br><br>

<img src="https://github.com/user-attachments/assets/fd6e0fd0-d687-4086-9337-ee7d5dd1efe4" width="700"><br>
<b>Figure 14.2.</b> Actual experimental setup of the PCM encoder and decoder system.

</div>

---

### Question 1

**Why does bandwidth limiting of the channel cause the PCM Decoder module to output incorrect voltages as well as the correct one?**

**Answer**

Bandwidth limiting attenuates the higher frequency components of the digital signal. These components are required to maintain sharp transitions between logic levels. When they are reduced, the waveform becomes distorted and the PCM decoder may incorrectly interpret the digital data, resulting in incorrect output voltages.

---

### Question 2

**If this were a communications system transmitting speech, what would these errors sound like when the message is reconstructed?**

**Answer**

The errors would appear as noise or distortion in the reconstructed speech signal. The audio may contain clicks, distortion, or irregular sound patterns due to incorrect decoding of the digital signal.

---

# Part B – Effects of Bandwidth Limiting on a Digital Signal’s Shape

In this part of the experiment, a **Sequence Generator module** is used to produce a digital bit pattern.

The signal is passed through a **Tunable Low-pass Filter**, which simulates a bandwidth-limited communication channel. The oscilloscope is used to observe how the waveform changes as the bandwidth is reduced.

<div align="center">

<img src="https://github.com/user-attachments/assets/4aa237ad-918e-4d01-bb9b-726aa0e60c24" width="700"><br>
<b>Figure 14.3.</b> Block diagram of the digital signal passing through the bandwidth-limited channel.

<br><br>

<img src="https://github.com/user-attachments/assets/637bf91f-38ec-45c1-b556-0016c4dd99db" width="700"><br>
<b>Figure 14.4.</b> Actual setup used to observe the distortion of the digital signal.

</div>

When the channel bandwidth is reduced:

- Bit transitions become **slower**
- The waveform becomes **distorted**

---

### Question 3

**What two things are happening to cause the digital signal to change shape?**

**Answer**

Two main effects cause the digital signal distortion:

1. **Attenuation of higher frequency harmonics**, which removes the components responsible for sharp transitions.
2. **Phase shift introduced by the filter**, which delays different frequency components by different amounts.

These effects combine to distort the digital waveform.

---

# Part C – Restoring Digital Signals

In this section, a **comparator circuit** is used to restore the distorted digital signal.

The comparator compares the distorted signal to a reference voltage and produces a clean digital output.

<div align="center">

<img src="https://github.com/user-attachments/assets/b90a6d5b-71c3-42b7-abdf-bbd18a7d1a75" width="700"><br>
<b>Figure 14.5.</b> Block diagram of the digital signal restoration system.

<br><br>

<img src="https://github.com/user-attachments/assets/2879c02b-973d-401b-bb44-77912b83fdbd" width="700"><br>
<b>Figure 14.6.</b> Experimental setup showing the comparator restoring the digital signal.

<br><br>

<img src="https://github.com/user-attachments/assets/3aeead2d-5bdf-4a08-b84d-5610dc3a5527" width="700"><br>
<b>Figure 14.7.</b> Restored digital signal output observed on the oscilloscope.

</div>

The comparator restores the digital signal by switching its output whenever the input crosses the reference voltage.

However, if the distortion is too severe, the restored signal may still contain errors.

---

# Conclusion

This experiment demonstrated how **bandwidth limitations affect digital communication systems**.

Reducing the channel bandwidth removes high-frequency components of digital signals, causing waveform distortion and potential decoding errors.

By using a **comparator circuit**, distorted signals can be partially restored to produce a clean digital output.

The experiment also illustrated how signal quality can be analyzed using oscilloscope observations and waveform analysis.
