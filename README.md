# 8051_ASM_code_electronicLock
This is a simple 8051F388 ASM code for a electronic lock using a 7 segments display and two buttons as the user interface

# How it works

The lock is supposed to start off with a default secure 4-digits key that is 4444 but you can change that to whatever digit between 0-9 that you want to when editing the code, after that you can use the K_SET button to navigate through the digits and K_LOAD to select one of them, if you enter the right password the lock unlocks and you have 2 options: 

1. You either press K_LOAD again and lock it with the same password.
2. Or you can wait 30 seconds and enter a new password and then lock it again.

If you enter the wrong password the lock will be locked for 30 seconds and then will allow you to try again, but should you fail more 2 times, besides the delay increasing 30 seconds each time, the lock will be permantly locked and will start to emit a signal, that can be used to sound an alarm, the only way to stop it is to reset the micro-controller therefore going back to the initial state.

# Other consideratons

I'm not a ASM programmer I'm simply a student so the code is not by any means perfect so feel free to improve the code if you want to!
Also, the Keil project might need to be re-configured for your specific micro-controller, in case you want to test it before you can use the Keil simulator to debug it and see what is happening under the hood.
