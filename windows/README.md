# Status for Windows
1. Download and unzip the windows zip file containing
    - red-dnd.bat
    - green-available.bat
    - blue-meeting.bat
    - purple-away.bat
2. Find the serial port of the LED
    - Open terminal (`⊞ + R`, type `cmd` and press `Enter`) and run `mode` to return the serial ports
    - Scroll until you see `Status for device COM##:`. This is the USB!
    - Copy the port name `COM##`  
    - add it to each of the command files by opening them in Notepad or similar and replacing `##`
3. Double click any batch file to see the status light change
