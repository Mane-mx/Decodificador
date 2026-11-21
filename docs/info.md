<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This circuit takes a 4-bit binary number from the input switches (IN0 to IN3) and shows the decimal number (0 to 9) on a 7-segment display.

IN0 is the least significant bit (value 1) and IN3 is the most significant bit (value 8). Inside, it uses basic logic gates (AND, OR, NOT) built from the truth table to turn on the right segments (OUT0 for segment a up to OUT6 for segment g). It does not need a clock signal because the output changes immediately when you flip a switch. If the binary input is greater than 9 (from 10 to 15), all outputs stay at 0 and the display turns off.

## How to test

1. Click the green Play button in Wokwi to start the simulation.
2. Leave all switches (IN0 to IN3) at 0 (0000). The display should show a 0.
3. Move the switches to test the binary numbers from 1 to 9:
	• 0001 (IN0 on) -> shows 1
	• 0010 (IN1 on) -> shows 2
	• 0011 (IN1 + IN0) -> shows 3
	• 0100 (IN2 on) -> shows 4
	• 0101 (IN2 + IN0) -> shows 5
	• 0110 (IN2 + IN1) -> shows 6
	• 0111 (IN2 + IN1 + IN0) -> shows 7
	• 1000 (IN3 on) -> shows 8
	• 1001 (IN3 + IN0) -> shows 9
4. Try any number above 9, for example 1010 (IN3 + IN1 on, which is 10) or 1111 (all on, 15). All segments should stay off.

## External hardware

List external hardware used in your project (e.g. PMOD, LED display, etc), if any
