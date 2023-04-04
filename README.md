# Status via fit statUSB
[Manufacturer Docs](http://fit-pc.com/wiki/index.php/Fit-statUSB)  
There are currently 4 status options  
- red (do not disturb)
- green (available)
- blue (in a meeting)
- purple (away)

## Windows Setup
1. Download and unzip the [Windows zip file](./windows/status-light.zip) containing
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
## Mac Setup
1. Download and unzip the [Windows zip file](./windows/status-light.zip) containing
    - red-dnd.command
    - green-available.command
    - blue-meeting.command
    - purple-away.command
2. Find the serial port of the LED
    - Open terminal and run `ls /dev`
    - Scroll until you see `/dev/cu.usbmodem####`
    - Get the ending number `####`
    - add it to the command files by opening in `nano` or similar code editor and replacing `##`
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

## Development
### Windows
- Fetch serial port automatically on startup
- Add port number to batch files automatically on startup
- Refactor into a light desktop app
### Mac
- Execute commands silently
- Fetch serial port automatically on startup
- Add port number to command files automatically on startup
- Preset the execute access
- Default open files with terminal (consider other filetypes)
- Refactor into a light MacOS app
### Slack Integration
Change status light depending on your slack status
- [Slack App - in dev](https://api.slack.com/apps/A04UG8CB3HS)
### Future Status Options
- Setting schedules
- RGB cycle (party)
- yellow
- yellow pulsing
- red-blue (police)
- random ("screensaver")
- pulse intervals
- pulsing between statuses