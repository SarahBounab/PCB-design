# Electrode–Skin Impedance Measurement System (AD5933-Based)
This project aims to measure **electrode–skin impedance** using different types of electrodes in order to determine which configuration provides the **lowest and most stable impedance** for bio-signal acquisition applications.

The system is based on the **AD5933 Evaluation Board**, a dedicated impedance spectroscopy platform. A custom analog front-end was designed to ensure safe current injection into biological tissue.

---

# Objective

* Measure electrode–skin impedance using **tetrapolar configuration**
* Compare different electrode types based on impedance performance
* Ensure **safe excitation current levels (human-safe bioimpedance testing)**

---

The system is divided into two main parts:

The measurement core is based on the **AD5933 Evaluation Board**, controlled via Analog Devices software.

* Performs impedance spectroscopy
* Requires calibration before measurement
* Provides frequency sweep excitation and impedance computation

---

To ensure safe and accurate measurements on human subjects, a dedicated analog conditioning circuit was designed.

* Stage 1: High-Pass Filter taht removes DC offset (1.48 V bias from voltage output)

* Stage 2: Voltage-to-Current Converter which is built using a **TL071** and converts excitation voltage into a **controlled constant current source**. Regulates injected current to **1 mA**

* Stage 3: Differential Voltage Sensing using **INA111**, it captures the voltage difference between sensing electrodes

* Stage 4: The Reference voltage of INA111 is set to **Vcc/2** to insures output is compatible with the **unipolar input range** of the AD5933 board

