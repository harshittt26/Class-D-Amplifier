# Class D Amplifier Project

A medium-power Class D amplifier designed using AutoCAD Eagle and simulated in LTspice.  
This project demonstrates how a low-voltage audio signal is modulated, converted into a PWM signal, amplified with high efficiency, and then filtered back into a high-power audio output.

---

## Project Overview
- **Design Software**: AutoCAD Eagle (circuit & PCB design)  
- **Simulation Software**: LTspice (circuit simulation & waveform analysis)  
- **Amplifier Type**: Class D (Switching Amplifier)  
- **Output Power**: Medium power (suitable for driving standard speaker loads)  

The design follows the typical signal flow of a Class D amplifier:
1. **Triangular Carrier Generation**  
2. **Audio Input (Sine Wave Modulation)**  
3. **PWM Generation via Comparator**  
4. **Output Switching Stage**  
5. **LC Filter for Audio Recovery**

---

## Typical Signal Parameters (Theoretical Working)

### 1. Triangular Wave (Carrier)  
The triangular wave acts as a high-frequency reference signal. It is compared with the input audio to generate a pulse-width modulated (PWM) signal. Its role is to ensure that the amplifier can translate the analog audio into varying pulse widths for efficient digital switching.

### 2. Audio Input (Sine Wave)  
The audio input provides the modulating signal that carries the sound information. When compared against the triangular carrier, the instantaneous amplitude of this sine wave determines the duty cycle of the PWM pulses.

### 3. PWM Signal (Comparator Output)  
The comparator produces a digital PWM waveform by comparing the triangular carrier with the audio input. The duty cycle of the output pulses varies in direct proportion to the input audio amplitude, effectively encoding the audio signal into time-domain variations.

### 4. Output Before Filtering  
At this stage, the amplifier output consists of a high-power PWM waveform. The signal still contains the high-frequency switching component but carries the audio information embedded within the pulse widths.

### 5. Filtered Audio Output  
An LC low-pass filter removes the high-frequency carrier, leaving only the amplified audio band. This produces a clean, high-power version of the original input audio signal, which is then fed to the loudspeaker.

---

## Building & Simulation

### AutoCAD Eagle
- Design schematic and PCB layout.  
- Define component footprints for power MOSFETs, drivers, and filter stage.  

### LTspice
- Simulate triangular wave generator, comparator stage, MOSFET drivers, and LC filter.  
- Observe signal waveforms at each stage:  
  - Triangle vs. audio at comparator  
  - PWM switching output  
  - Filtered audio waveform at load  

---

## License
This project is released under the **MIT License**.  
Free for academic and personal use.  


---

## Circuit Diagram

Below is the circuit block diagram of the designed Class D Amplifier:

![Class D Amplifier Circuit](WhatsApp%20Image%202025-10-03%20at%2012.59.26%20AM.jpeg)
