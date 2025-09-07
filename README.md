# PitchPerfect
An app that detects pitch and identifies musical notes in real time.

Pitch Perfect is an app that detects what note you’re playing (or what key you’re in) with any instrument.

<img width="828" height="1792" alt="IMG_0703" src="https://github.com/user-attachments/assets/5e561663-6d00-4adc-9971-6cbb88f25c0e" />

<img width="828" height="1792" alt="IMG_0707" src="https://github.com/user-attachments/assets/4a8b3696-36c3-45d8-809c-f24e7406bc1d" />

How it works:
•	The app listens to your microphone and measures the sound’s frequency.
•	Every musical note has a “home frequency.” For example:
A4 = 440 Hz
C4 ≈ 261.63 Hz
C♯4 ≈ 277.18 Hz
D4 ≈ 293.66 Hz

•	Using zero-crossings, the app counts how many times the sound wave repeats per second.
Example: If it repeats ~277 times per second, that’s 277 Hz.

•	It then compares the measured frequency to the note map:
o	C4 = 261.63 Hz (too low)
o	C♯4 = 277.18 Hz (closest match)
o	D4 = 293.66 Hz (too high)
So the closest match is C♯4.

In short:
1.	Detects the base frequency of the sound.
2.	Matches it to the nearest musical note.
3.	Reports which note it is and how far off you are (sharp or flat).
