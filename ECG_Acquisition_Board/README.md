# ECG Acquisition Board

This project presents a custom PCB designed for **ECG signal acquisition and conditioning**.
The board was developed to acquire low-amplitude cardiac signals and condition them for accurate visualization.
The system operates using a **dual power supply**.

---

# Architecture

The board is divided into several functional blocks:

* The acquisition stage : is based on the **INA122 instrumentation amplifier** for low-amplitude biosignal acquisition
 The component was selected for its:
  * High Common Mode Rejection Ratio (CMRR)
  * Low offset voltage
  * Adjustable gain configuration

A preamplification gain of approximately **200 ** was implemented in order to amplify the weak ECG signal while minimizing common-mode noise.

---

* A high-pass filter was designed to remove DC components and baseline drift from the ECG signal with a cutoff frequency of **0.5 Hz**.

---

* A low-pass filter was implemented to attenuate high-frequency noise while preserving the useful ECG signal bandwidth with a cutoff frequency of **100 Hz**.


---

* A non-inverting amplification stage based on the **TL082 operational amplifier** was added to further amplify the conditioned ECG signal with **a voltage gain of 20.**

---


# Components Used

* INA122 instrumentation amplifier
* TL082 operational amplifier
* External ADC module (since the ESP's ADC attinuated the negative part of the ECG signal)


