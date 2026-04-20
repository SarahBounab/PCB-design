# Overview
This PCB is designed for the acquisition and conditioning of EMG signals from the pectoralis muscle. The system operates on a single supply and is structured into three main functional blocks: preamplification, signal processing, and final amplification.

---

* The first stage is responsible for capturing low-amplitude EMG signals and amplifying them while minimizing noise.
 INA122 instrumentation amplifier was used because of its 
  * Low input offset voltage
  * High Common Mode Rejection Ratio (CMRR)
  * Wide gain range
After experimental tuning, an optimal **preamplification gain of 500** was selected to ensure a good balance between signal quality and noise amplification.

---

The second stage which is signal processing stage performs analog filtering to isolate the useful EMG frequency band and remove unwanted components.
TL082 operational amplifier was used to perform
* **High-pass filtering (~30 Hz):**
  Removes DC components, motion artifacts, and ECG interference (QRS complex)
* **Low-pass filtering (~500 Hz):**
  Eliminates high-frequency noise
* **Notch filter (50 Hz):**
  Suppresses power line interference
 Final retained bandwidth: **30 Hz – 500 Hz**

---

The final stage which is the amplification stage increases the signal amplitude with a non inverting configuration and a * **Gain:** 201

---




