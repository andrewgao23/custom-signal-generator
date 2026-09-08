## Waveform Simulation

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
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/47398c6e-c93b-4331-a100-67d59df55b6d" />
<br><br>
(Above) Output waveforms without push-pull amplifier.
<br><br>
<img width="1917" height="846" alt="image" src="https://github.com/user-attachments/assets/bb002dca-314c-419f-b504-605fe2ca195d" />
<br><br>
(Above) Output waveforms side by side (blue: with push-pull amp, green: without). It seems that the push-pull amp distorts the waveform slightly in the middle.
<br><br>
<img width="1917" height="846" alt="image" src="https://github.com/user-attachments/assets/812ff5a1-c53f-495f-b73d-96328493a5e6" />
<br><br>
(Above) Current draw out of the amplifier op-amp with (blue) and without (green) push-pull amp. The push-pull amp supplies current, meaning the op-amp does not have to handle as much current.

## Relaxation Oscillator Breakdown

<img width="1917" height="887" alt="image" src="https://github.com/user-attachments/assets/bb9b099a-b79b-4b65-9206-0c8f8562dfca" />
<br><br>
(Above) Square + triangle wave outputs when R1 is changed from 100K -> 50K.
<br><br>
<img width="1917" height="841" alt="image" src="https://github.com/user-attachments/assets/70c354e4-e1e9-47fc-8818-4fb5243cb81d" />
<br><br>
(Above) Square + triangle wave outputs when R1 is short circuited.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/f19ccd7f-b4e1-4bba-80e6-e49638dc9ff3" />
<br><br>
(Above) Square + triangle wave outputs when R2 is changed from 100K -> 65.7K.
<br><br>
<img width="1917" height="847" alt="image" src="https://github.com/user-attachments/assets/0daba1a7-2e1b-45c7-b823-fd982e8f8f98" />
<br><br>
(Above) Square + triangle wave outputs when R2 is changed from 100K -> 65.6K. There seems to be a threshold in between 65.6K and 65.7K that causes the waveform to completely collapse if the resistance of R2 crosses that threshold.
<br><br>
<img width="1915" height="842" alt="image" src="https://github.com/user-attachments/assets/223f2710-bd3d-404b-9ea0-5b733c767d88" />
<br><br>
(Above) Square + triangle wave outputs when R2 is short circuited. When both R1 and R2 are short circuited, square and triangle wave outputs stay at 0.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/4d9edae1-9809-4d2e-89ab-d7f4335ea151" />
<br><br>
(Above) Square output when R3 is changed from 5.1K -> 5K. (Green is 5K, Blue is 5.1K). Output is phase shifted 180 degrees at any resistance below 5.1K, and remains at the same phase for any resistance above 5.1K.
<br><br>
<img width="1917" height="866" alt="image" src="https://github.com/user-attachments/assets/faf32d2f-390d-4cfc-8633-910c5c7563ae" />
<br><br>
(Above) Square + triangle outputs when D1 is short circuited.
<br><br>
<img width="1917" height="847" alt="image" src="https://github.com/user-attachments/assets/c5a9a568-a3a8-43be-a434-5e114156fbc2" />
<br><br>
(Above) Square + triangle outputs when D2 is short circuited.
<br><br>

## Diode Wave Shaper Breakdown

<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/2298efe9-5130-4fae-9dd6-27d246205093" />
<br><br>
(Above) Wave shaper output when R5 is changed from 3.2K -> 5K.
<br><br>
<img width="1917" height="847" alt="image" src="https://github.com/user-attachments/assets/ca642cc8-b763-4003-9af0-17360eb17ff4" />
<br><br>
(Above) Wave shaper output when R5 is short circuited.
<br><br>
<img width="1917" height="846" alt="image" src="https://github.com/user-attachments/assets/ba5f7706-c3fa-4e80-ad5b-45fdaaf3b8d6" />
<br><br>
(Above) Wave shaper output when R6 is changed from 1.8K -> 0.9K.
<br><br>
<img width="1917" height="841" alt="image" src="https://github.com/user-attachments/assets/582e830b-23d4-4f47-b44f-f096b7ff91db" />
<br><br>
(Above) Wave shaper output when R6-ground node is removed.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/a4c7e828-d4e7-48c2-9268-d98e99645623" />
<br><br>
(Above) Wave shaper output when R7 is changed from 3.2K -> 1.6K.
<br><br>
<img width="1917" height="848" alt="image" src="https://github.com/user-attachments/assets/d6d61f23-4691-4967-b787-482039aa13fa" />
<br><br>
(Above) Wave shaper output when R7 is changed from 3.2K -> 5K.
<br><br>
<img width="1917" height="850" alt="image" src="https://github.com/user-attachments/assets/8fbe763d-5bbf-40b2-9759-0dda136bf334" />
<br><br>
(Above) Wave shaper output when R7 is short circuited.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/c1a9e7dd-a347-4ee4-8439-845a2fe42793" />
<br><br>
(Above) Wave shaper output when D3 is short circuited.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/1dd7b200-6b7c-454f-9e11-b6c9aa81a2f1" />
<br><br>
(Above) Wave shaper output when D4 is short circuited.
<br><br>
<img width="1917" height="845" alt="image" src="https://github.com/user-attachments/assets/507e88e7-2e6a-4318-8686-737294910029" />
<br><br>
(Above) Wave shaper output when D5 is short circuited. (Same result for D6).
<br><br>
<img width="1917" height="847" alt="image" src="https://github.com/user-attachments/assets/1a65a775-5eff-41f8-940b-e37b45aa7db0" />
<br><br>
(Above) Wave shaper output when D7 is short circuited. (Same result for D8).
<br><br>
<img width="1917" height="846" alt="image" src="https://github.com/user-attachments/assets/bc935d63-bc80-4e0a-87c7-a9abc7a6d747" />
<br><br>
(Above) Wave shaper output when the D5-D6-ground node is removed.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/bff41d57-8aab-44a0-a85d-406c079b04e5" />
<br><br>
(Above) Wave shaper output when the D7-D8-ground node is removed.
<br><br>
<img width="1917" height="842" alt="image" src="https://github.com/user-attachments/assets/a57e8475-e56b-4f02-b98c-8364f3f0c9a8" />
<br><br>
(Above) Wave shaper output when the D3-D4-R7-ground node is removed.
