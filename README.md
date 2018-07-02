This is a guide on how to get your Fridge Scan running on your Raspberry Pi 3

What you will need:
Raspberry Pi 3
Elegoo Touchscreen LCD
USB Laser Barcode scanner
16GB Micro SD Card

Step 1 Setup:
Plug your USB Scanner into you Pi.
Boot it while the scanner is connected.
Connect your Pi with the internet
  - An ethernet cable or WiFi are both fine.
Open the terminal.
Find out what size your Elegoo touchscreen LCD is.
Type "sudo raspi-config" in your terminal.
Enable "Serial" at the interfacing options.

Step 2 Installing dependencies:
Type "pip install requests" in your terminal.
Type "sudo rm -rf LCD-show" in your terminal.
Type "git clone https://github.com/goodtft/LCD-show.git" in your terminal.
Type "chmod -R 755 LCD-show" in your terminal.
Type "cd LCD-show/" in your terminal.
Replace ** with the 2 digits of your Elegoo LCD screen size and type "sudo ./LCD**-show" in your terminal.
These commands will take a while to finnish.

Step 3 Reboot:
Turn off your Pi.
Connect the LCD screen to the Raspberry.
Turn on your pi.

Step 4 Code:
Download the Barcode.py from this github on your Pi.
This can be easilly done by using the build-in Pi browser.
Open your terminal.
Type "sudo python barcode.py" to run your script.
Enjoy yuor fridge scan!

Step 5 (optional):
Navigate to https://upcdatabase.org/ and get your own API key.
Edit line 6 of your code with your own API key.
This can be handy if you have reached the lookup limit in the UPC database.
