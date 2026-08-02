# custom-signal-generator
An op-amp based analog signal generator that accepts a 24V DC input and produces a 5V sine wave output, with configurable gain, frequency, and wave shape. Also supports square + triangle waveform outputs. Schematic and PCB layout designed in Altium and simulated in LTSpice.
<img width="1441" height="827" alt="image" src="https://github.com/user-attachments/assets/0fb30d8c-4771-4cb5-8360-34de4467dbe2" />

## Components
- [Relaxation Oscillator](#relaxation-oscillator)
- [Diode Wave Shaper](#diode-wave-shaper)
- [Amplifier](#amplifier)
- [Push-Pull Amplifier](#push-pull-amplifier)

## Relaxation Oscillator
<img width="1482" height="791" alt="image" src="https://github.com/user-attachments/assets/f4aa0bfa-2a60-4425-81e9-00f1a92dd363" />
The LM741 (U1) is wired as a comparator with positive feedback (R1/R2) to produce the square wave output. That square wave feeds through a 5.1K resistor into a node clamped by a pair of zener diodes (D1/D2) and trimmed by potentiometer TR1, which sets the charge/discharge behavior into U2. U2 is configured as an integrator through a 1nF capacitor (C1), which converts the square wave into the triangle wave output. TR1 adjusts waveform frequency.
## Diode Wave Shaper
<img width="1320" height="728" alt="image" src="https://github.com/user-attachments/assets/09c16bed-7a2f-463c-a3f3-f2eee61f048d" />
Takes the triangle wave through R6/R7 into a ladder of diode branches (D3–D8), each connected to ground through a different resistor combination (R9–R13). As the triangle wave's voltage rises, each diode branch turns on at a progressively higher threshold, adding a new parallel resistive path to ground at that point. Diodes D3, D5 and D6 curve the waveform when voltage is >0, and diodes D4, D7 and D8 curve the waveform when voltage is <0.
## Amplfiier
<img width="682" height="701" alt="image" src="https://github.com/user-attachments/assets/042b4dcf-7c57-4867-be3a-a21954453b88" />
A third LM741 (U3) buffers and adjusts the gain of the shaped waveform before it reaches the output stage, with potentiometer TR2 and resistor R14 setting the adjustable gain level.
## Push Pull Amplifier
<img width="855" height="667" alt="image" src="https://github.com/user-attachments/assets/6c5d4277-f59b-41bf-b9ae-be124ceb8c45" />
Not strictly necessary, but useful for OCP. One transistor sources current on the positive half of the waveform, the other sinks it on the negative half. C2 couples the output.

## Simulation
- AC and transient simulations through LTSpice test points validating gain, frequency, wave shape + configurability through potentiometers

## Approach
- Wein Bridge not feasible for configurable frequency due to fixed capacitor necessary for waveform




