# Ubuntu Linux Instructions
Welcome DIY adventure penguins! 🐧
1. Install minicom ([doc](https://help.ubuntu.com/community/Minicom)) `sudo apt-get install minicom`
2. Find the serial port name `dmesg | grep tty` and copy it for step 3 (eg. ttyS0 or ttyACM0)
3. `sudo minicom -s`, choose `A - Serial Device` and set it to `/dev/[INSERT_SERIAL_PORT]`
4. Exit minicom via `ctrl + A` then `X`, then run `sudo minicom` then simply enter `#hexcode` to change status
    - Red (DND) `B#FF0000-0600#000000-0200`
    - Green (available) `#00FF00`
    - Purple (away) `#FF0066`
    - Blue (meeting) `#00FFFF`
