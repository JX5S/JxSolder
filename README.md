# Do not order the board, or blindly copy the design, there are several known issues. Namely:
- USB-PD doesn't work. I though I could do dead battery the way I did, but it's not a good way to do it, use PA9 and PA10 instead
- Display reset needs to be wired via an RC filter to 3.3V
- Vref needs to be connected up
- Button logic is flipped - so DFU firmware upload doesn't work
- There are unidirectional transils on the input - which blow up when incorrect polarity is plugged in. Should be replaced by bidirectional transils, the ideal diodes will protect the input
