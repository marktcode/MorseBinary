#Morse-code to Binary-code mapping

The code mapping contained in the file enigma.tex enables Morse code to be used to transmit 
arbitrary binary sequences... Care has to be taken with the way the end of an encoding is handled 
since it is unlikely to neatly coincide with a Morse lettery. 

If for example the binary string is an exact number of bytes then one way to manage this is 
to add to the string a run-out sequence 11100000 to the tail end of the intended binary and then   
perform an adjustement at the receiving end to peal of any surplus bits beyond a rounded byte count.
If the received string is a whole number of bytes then the last byte should be rmoved.

Examples of this mapping to be found in cmprs_morse and dcmprs_morse in:
https://github.com/marktcode/tcodetools-for-Raspberry-Pi-or-mac/tree/main/MsgCompressor 