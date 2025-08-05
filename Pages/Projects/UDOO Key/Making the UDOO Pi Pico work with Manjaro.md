---
dg-publish: true
---

Fun little quirks I've learned through this process:
- Have to either click "Mount and open" while compiling if it pops up or set it to automount on connection. The weird thing is it only does so after being sent a certain signal by the compiler.
- Remember to have something logging every now and again as a sanity check - after coming back to this project after a little while I kept connecting to the serial port, seeing nothing and disconnecting - later only to realise it had no print statements on that serial port.
- Make sure to disconnect from the serial port before mounting with the compiler and loading the program (this might only matter for the ESP32 though).