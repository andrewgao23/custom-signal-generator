# custom-signal-generator
An op-amp based analog signal generator that accepts a 24V DC input and produces a 5V sine wave output, with configurable gain, frequency, and wave shape. Also supports square + triangle waveform outputs. Schematic and PCB layout designed in Altium and simulated in LTSpice.
<br><br>
<img width="1441" height="827" alt="image" src="https://github.com/user-attachments/assets/0fb30d8c-4771-4cb5-8360-34de4467dbe2" />
<br><br>

## Components
- [Relaxation Oscillator](#relaxation-oscillator)
- [Diode Wave Shaper](#diode-wave-shaper)
- [Amplifier](#amplifier)
- [Push-Pull Amplifier](#push-pull-amplifier)
<br><br>

## Relaxation Oscillator
<img width="1482" height="791" alt="image" src="https://github.com/user-attachments/assets/f4aa0bfa-2a60-4425-81e9-00f1a92dd363" />
<br><br>
The LM741 (U1) is wired as a comparator with positive feedback (R1/R2) to produce the square wave output. That square wave feeds through a 5.1K resistor into a node clamped by a pair of zener diodes (D1/D2) and trimmed by potentiometer TR1, which sets the charge/discharge behavior into U2. U2 is configured as an integrator through a 1nF capacitor (C1), which converts the square wave into the triangle wave output. TR1 adjusts waveform frequency.
<br><br>

## Diode Wave Shaper
<img width="1320" height="728" alt="image" src="https://github.com/user-attachments/assets/09c16bed-7a2f-463c-a3f3-f2eee61f048d" />
<br><br>
Takes the triangle wave through R6/R7 into a ladder of diode branches (D3–D8), each connected to ground through a different resistor combination (R9–R13). As the triangle wave's voltage rises, each diode branch turns on at a progressively higher threshold, adding a new parallel resistive path to ground at that point. Diodes D3, D5 and D6 curve the waveform when voltage is >0, and diodes D4, D7 and D8 curve the waveform when voltage is <0. If needed, resistors R11-R13 can be adjusted to fine-tune waveform shape.
<br><br>

## Amplifier
<img width="682" height="701" alt="image" src="https://github.com/user-attachments/assets/042b4dcf-7c57-4867-be3a-a21954453b88" />
<br><br>
A third LM741 (U3) buffers and adjusts the gain of the shaped waveform before it reaches the output stage, with potentiometer TR2 and resistor R14 setting the adjustable gain level.
<br><br>

## Push Pull Amplifier
<img width="855" height="667" alt="image" src="https://github.com/user-attachments/assets/6c5d4277-f59b-41bf-b9ae-be124ceb8c45" />
<br><br>
Not strictly necessary, but useful for OCP. One transistor sources current on the positive half of the waveform, the other sinks it on the negative half. C2 couples the output.
<br><br>

## Simulation

<img width="1917" height="870" alt="image" src="https://github.com/user-attachments/assets/683eb11d-61fa-4113-be10-d55a0224e99b" />
<br><br>
(Above) Sine wave, triangle wave, and square wave outputs at respective test points.
<br><br>
<img width="1917" height="871" alt="image" src="https://github.com/user-attachments/assets/6a7ab2fa-9c5d-4a0b-989b-93b0ae88e3e2" />
<br><br>
(Above) Output waveforms when TR1 is adjusted (100K -> 50K).
<br><br>
<img width="1917" height="877" alt="image" src="https://github.com/user-attachments/assets/90ed579d-eed4-4f72-8a0a-e77149f938db" />
<br><br>
(Above) Output waveforms when R11-R13 equivalent resistance is adjusted (1.8K -> 3.2K).
<br><br>
<img width="1917" height="877" alt="image" src="https://github.com/user-attachments/assets/b3727d77-5153-4bbe-90ff-49592803473c" />
<br><br>
(Above) Output waveforms when TR2 is adjusted (3.5K -> 1.5K). Vout clips at 6V.
<br><br>

## Approach

<img width="818" height="733" alt="image" src="https://github.com/user-attachments/assets/5746e3e9-6d70-4e52-8cb4-79ccf43e9eb3" />
<br><br>
The Wein Bridge oscillator was a potential option but not feasible due to a variable capacitance being necessary for a configurable frequency, if a sinusoidal output waveform were to be preserved.




