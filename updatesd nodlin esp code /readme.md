## This is to solve the emergency stop problem faced in the previous update 3 folder, and this has smooth servo control 

In  the previous update 3 code, when executing the memory save operations and then pressing the emergency stop, it doesn't work properly .

### Right now, your E-Stop is failing for two reasons:

    The JavaScript Loop: Once you hit "Execute," JavaScript locks into a for loop and rapidly fires off all the saved commands. It doesn't know how to "break" out of that loop if you press a different button.
    
    The Hardware Sweep: Even if you stopped JavaScript, your ESP8266 is running that asynchronous background sweep we just added. If it was halfway to 180°, it will finish the sweep even if the website goes silent.
