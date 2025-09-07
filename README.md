# PitchPerfect
An app that detects pitch and identifies musical notes in real time.

Pitch Perfect is an app that detects what note you’re playing (or what key you’re in) with any instrument.

How it works:
•	The app listens to your microphone and measures the sound’s frequency.
•	Every musical note has a “home frequency.” For example:
o	A4 = 440 Hz
o	C4 ≈ 261.63 Hz
o	C♯4 ≈ 277.18 Hz
o	D4 ≈ 293.66 Hz

•	Using zero-crossings, the app counts how many times the sound wave repeats per second.
o	Example: If it repeats ~277 times per second, that’s 277 Hz.

•	It then compares the measured frequency to the note map:
o	C4 = 261.63 Hz (too low)
o	C♯4 = 277.18 Hz (closest match)
o	D4 = 293.66 Hz (too high)
So the closest match is C♯4.

In short:
1.	Detects the base frequency of the sound.
2.	Matches it to the nearest musical note.
3.	Reports which note it is and how far off you are (sharp or flat).
