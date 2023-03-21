# Status for Windows
Automate this process in an exe file
1. Find the serial port of the LED (this doesn't change on windows if the LED is unplugged)
    - Open terminal and run `mode` to return the serial ports
    - Scroll until you see `Status for device COM##:`. This is the USB (RUN ON STARTUP OR HAVE A PORT LISTENER)
    - Get the port name `COM##`  
    - add it to the command files

2. Download the status batch files (ONE-TIME)
    - red-dnd.bat
    - green-available.bat
    - blue-meeting.bat
    - purple-away.bat
3. TODO: RUN IN TERMINAL
4. TODO: RUN ON CLICK
