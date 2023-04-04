# Status for Mac
1. Download the zip file containing
    - red-dnd.command
    - green-available.command
    - blue-meeting.command
    - purple-away.command
2. Find the serial port of the LED
    - Open terminal and run `ls /dev`
    - Scroll until you see `/dev/cu.usbmodem####`
    - Get the ending number `####`
    - add it to the command files by opening in `nano` or similar code editor
3. Give executing access to each command
    - In terminal, `cd` the directory containing the command files
        - `chmod a+x red-dnd.command`
        - `chmod a+x green-available.command`
        - `chmod a+x blue-meeting.command`
        - `chmod a+x purple-away.command`
4. Set up the files to always open in terminal
    - In the File Explorer, select `options` and then `open with`, then select `terminal`
    - Click yes through the following popups
5. Double click any command file to see the status light change
    - The command does not currently execute silently, a terminal window opens every time a command is clicked. These can be closed at any time.
