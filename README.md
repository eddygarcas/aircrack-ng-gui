# aircrack-ng GUI

A basic aircrack-ng gui interface using python-gtk3

## What can it do?
Initially, it is to support airmon-ng, where the user can start, stop and check the status of airmon-ng. | **Completed**

Access points scanning window using "iw" with automatic bssid and channel extraction after user chooses an ssid to be attacked. | **Completed**

Airodump-ng with a running timeout, user can choose the access point, specifiy for how long should airodump-ng listen to its trafic, and it will output the data in .cap format | **Completed** * also still looking for a way to autodetect the handshake and terminate airodump-ng

Aircrack-ng window where the user can select a wordlist and the cap file that has the handshake, then the script will try to bruteforce the ap using the wordlist | **Completed**

## Screenshots

### Main Window
Main Window where user can choose to go Scan|airmon-ng|aircrack-ng windows after selecting the interface (wlp4s0)

![Alt text](1.png?raw=true "ScreenShot 1")

### Airmon-ng  Window
A window to check|start|stop airmon-ng, along with starting|stopping systemd NetworkManager.service

![Alt text](9.png?raw=true "ScreenShot 9")

### Scanning Window
A wifi access point scanning window. After choosing their interface, the user can scan for wifi ap using iw. Then, after choosing the target ap, they can go to airodump-ng after starting airmon-ng

![Alt text](2.png?raw=true "ScreenShot 2")

### Airmon-ng "with ssid chosen window" Window
Very similar to Airmon-ng window, except this one pass the ssid variables "SSID, BSSID, CHANNEL" to Airodump-ng window

![Alt text](3.png?raw=true "ScreenShot 3")

### Airodump-ng Window | 1
To run airodump-ng (via desired terminal emulator) on the targeted SSID and output the file (with the handshake) to a desired file name. | (could be done better using STDERR and subprocess)

![Alt text](5.png?raw=true "ScreenShot 5")



### Airodump-ng Window | 2
After running airodump-ng, the user can use aireplay to send deauthentication packets for desired n times and a desired station to capture the handshake

![Alt text](6.png?raw=true "ScreenShot 6")

### Aircrack-ng Window
After saving the handshake into a cap file, aircrack can be accessed from the main window. The user chooses a .cap file that contain the handshake and a wordlist to perform the bruteforce attack on their desired terminal emulator.

![Alt text](8.png?raw=true "ScreenShot 8")
