# Status for Mac
Automate this process in an exe file
1. Find the serial port of the LED (this may change if the LED is unplugged)
    - Open terminal and run `ls /dev`
    - Scroll until you see `/dev/cu.usbmodem####`
    - Get the ending number `####`  (RUN ON STARTUP OR HAVE A PORT LISTENER)
    - add it to the command files

2. Download the status command files (ONE-TIME)
    - red-dnd.command
    - green-available.command
    - blue-meeting.command
    - purple-away.command
3. Open terminal and `cd` the directory containing the command file
4. Run `chmod a+x STATUS_NAME.command` to give execute access to the command