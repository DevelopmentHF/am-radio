# Requirements

## 1. Project Objective

Design and build a fully functional analog AM superheterodyne radio.

The system shall receive medium-wave AM broadcast signals through an antenna, select and frequency-convert the desired station, demodulate the received AM signal, amplify the recovered audio, and drive either headphones or a loudspeaker.

The electrical system shall be implemented on a custom PCB and integrated into a custom mechanical enclosure.

---

## 2. Functional Requirements

### RF Reception

**REQ-RF-001**  
The radio shall receive amplitude-modulated (AM) broadcast signals in the medium-wave frequency range.

**REQ-RF-002**  
The radio shall be capable of receiving a carrier at **693 kHz**.

**REQ-RF-003**  
The radio shall be tunable to multiple AM broadcast frequencies rather than being fixed exclusively to 693 kHz.

**REQ-RF-004**  
The radio shall use a ferrite-rod or equivalent medium-wave receiving antenna.

**REQ-RF-005**  
The receiver shall include a tunable RF-selective network capable of selecting the desired station while attenuating signals outside the selected channel.

---

## 3. Receiver Architecture

**REQ-RX-001**  
The receiver shall use a **superheterodyne architecture**.

The nominal signal path shall consist of:

Antenna  
→ RF tuning / filtering  
→ RF amplification  
→ Frequency mixer  
→ Intermediate-frequency filtering  
→ Intermediate-frequency amplification  
→ AM detection  
→ Audio-frequency amplification  
→ Audio output

**REQ-RX-002**  
The receiver shall contain a local oscillator suitable for frequency conversion of the selected RF signal to a fixed intermediate frequency.

**REQ-RX-003**  
The receiver shall use a fixed intermediate frequency selected during the design process.

**REQ-RX-004**  
The mixer and local oscillator shall frequency-convert each selected station to the chosen intermediate frequency.

**REQ-RX-005**  
The IF stage shall provide sufficient filtering to discriminate between the desired signal and unwanted mixer products / adjacent signals.

**REQ-RX-006**  
The receiver shall provide sufficient RF and/or IF gain for received broadcast signals to be demodulated reliably.

---

## 4. AM Demodulation

**REQ-DEM-001**  
The receiver shall demodulate conventional amplitude-modulated broadcast signals.

**REQ-DEM-002**  
The detector shall recover the audio-frequency modulation while substantially rejecting the RF/IF carrier component.

**REQ-DEM-003**  
The demodulated signal shall preserve intelligible speech and broadcast audio without significant audible distortion under normal reception conditions.

---

## 5. Audio System

**REQ-AUD-001**  
The radio shall include an audio-frequency amplification stage after demodulation.

**REQ-AUD-002**  
The user shall be able to control audio output volume.

**REQ-AUD-003**  
The radio shall provide an audio output capable of driving at least one of the following:

- an integrated loudspeaker;
- headphones.

**REQ-AUD-004**  
If an integrated loudspeaker is used, the audio output stage shall provide sufficient power to produce clearly audible sound in a normal indoor environment.

---

## 6. User Controls

**REQ-UI-001**  
The radio shall provide a user-accessible station tuning control.

**REQ-UI-002**  
The radio shall provide a user-accessible volume control.

**REQ-UI-003**  
The radio shall provide a means of switching power on and off.

**REQ-UI-004**  
The tuning mechanism shall cover the intended AM reception frequency range without requiring modification of the PCB or components.

---

## 7. Power

**REQ-PWR-001**  
The radio shall operate from a low-voltage DC power source.

**REQ-PWR-002**  
The power architecture shall provide suitable supply voltages for the RF, IF, demodulation, and audio stages.

**REQ-PWR-003**  
The design shall include local supply decoupling appropriate to the requirements of the RF and audio circuitry.

**REQ-PWR-004**  
RF/IF circuitry shall be protected, where necessary, from noise or instability caused by the audio power stage and power supply.

---

## 8. PCB

**REQ-PCB-001**  
The final electrical design shall be implemented on a custom PCB.

**REQ-PCB-002**  
The PCB shall contain the receiver signal-processing chain and audio electronics required for normal operation.

**REQ-PCB-003**  
External components such as the antenna, speaker, tuning controls, and power source may connect to the PCB using suitable connectors or wiring.

**REQ-PCB-004**  
The PCB shall include labelled test points at important locations within the signal chain where practical.

Candidate test points include:

- RF input / tuned RF output;
- local oscillator;
- mixer output;
- IF output;
- detector output;
- audio amplifier output.

**REQ-PCB-005**  
The PCB layout shall account for RF signal integrity, grounding, supply decoupling, and isolation between sensitive RF stages and high-current audio circuitry.

---

## 9. Mechanical Design

**REQ-MECH-001**  
The completed radio shall be installed within a custom-designed enclosure.

**REQ-MECH-002**  
The enclosure shall provide mechanical mounting for the PCB, antenna, speaker, controls, and power hardware.

**REQ-MECH-003**  
Tuning, volume, and power controls shall be accessible when the enclosure is assembled.

**REQ-MECH-004**  
The enclosure shall include an appropriate opening or grille for the loudspeaker if a speaker is fitted.

**REQ-MECH-005**  
The enclosure design shall allow the radio to be assembled and disassembled without damaging the PCB or wiring.

---

## 10. Simulation

**REQ-SIM-001**  
Major analog functional blocks shall be simulated in LTspice before PCB manufacture.

These shall include, where applicable:

- AM signal source;
- antenna / RF tuned circuit;
- RF amplifier;
- local oscillator;
- mixer;
- IF filter;
- IF amplifier;
- AM detector;
- audio amplifier.

**REQ-SIM-002**  
An integrated LTspice simulation shall be developed for as much of the complete receiver signal chain as practical.

**REQ-SIM-003**  
Simulation shall be used to verify the frequency response and operation of each major receiver stage before hardware implementation.

---

## 11. Verification and Testing

**REQ-TEST-001**  
Each major receiver block shall be testable independently where practical.

**REQ-TEST-002**  
The RF tuned circuit shall demonstrate a measurable response peak at the selected station frequency.

**REQ-TEST-003**  
The local oscillator frequency shall be measured and verified against the frequency required to produce the chosen IF.

**REQ-TEST-004**  
The mixer shall be verified to produce the intended intermediate-frequency component from the selected RF and LO inputs.

**REQ-TEST-005**  
The IF filtering stage shall demonstrate preferential transmission of the chosen intermediate-frequency band.

**REQ-TEST-006**  
The detector shall recover a known audio modulation signal from a laboratory-generated AM input.

**REQ-TEST-007**  
The complete receiver shall successfully reproduce intelligible audio from a real **693 kHz AM broadcast signal**.

**REQ-TEST-008**  
The complete receiver shall demonstrate reception of at least one additional AM broadcast frequency within its designed tuning range.

---

## 12. Documentation

**REQ-DOC-001**  
Major design decisions shall be documented and assigned traceable decision identifiers.

**REQ-DOC-002**  
Relevant calculations shall be recorded and linked to the requirements or design decisions they support.

**REQ-DOC-003**  
LTspice simulations shall be retained alongside the project source.

**REQ-DOC-004**  
Schematic and PCB revisions shall be maintained using Git.

**REQ-DOC-005**  
Verification results shall be recorded against the corresponding requirements.

**REQ-DOC-006**  
The final project documentation shall include:

- system architecture;
- design decisions;
- calculations;
- schematic;
- PCB design;
- bill of materials;
- mechanical design;
- simulation results;
- hardware test results.