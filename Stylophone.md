555 timer:  
Astable mode

Playing Notes:  
Metal plates connected to resistors (potentionmeters or specific resistors)  
Connect each note (resistor) in series into the stylus

Resistor values:  
Constant resistor between pin 8 and 7 should be around 1kohm to not mess up resistance of notes

f \= 1.44/((constantResistor \+ 2\*notesResistors) \* C)

notesResistors \= 1.44/(2\*f\*C) \- constantResistor/2

Octave switching:  
A simple octave switch requires simply adding a potentiometer before the timer circuit to lower or increase the baseline resistance

A true octave switch means, switching the timing capacitor values

Use LM358P op amp with a capacitor to smoothen out the frequency from the 555 output

Keep Pin 5 (control voltage) connected to gnd through a 10nF capacitor

the first “resistor” is actually the fixed resistor at 1kohm  
The second resistor in parallel with the diode is actually the combined resistance of music notes  
The stylus is a disconnection at the intersection between pin 2 and the second resistor so it touches the “second resistor”  
Timing capacitor is 100nF  
<img width="224" height="333" alt="image" src="https://github.com/user-attachments/assets/27d26004-88f6-416f-8e09-71ac0cc728f5" />

Octave Potentiometer goes between pin 7 and music resistor

After pin 3 (output):  
In series with a 10uF capacitor  
Goes to 10k Linear pot (volume)  
Goes to IN+ of LM358 from wiper  
From LM358 output to 10nF capacitor (filter cap) and IN- for gain  
Finally to speaker from filter cap  
