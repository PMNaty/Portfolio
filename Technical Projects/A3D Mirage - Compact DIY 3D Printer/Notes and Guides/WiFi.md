## Switching WiFi / Connecting to WiFi

**Goals:**<br>
1.) To connect to an existing WiFi network and get the IP address to access the Mainsail page.<br>
2.) To switch WiFi networks.

*The WiFi connection automatically switches to a different known network when it cannot connect to the main one*

Reference: [Siboor V0.2 Tutorial](https://docs.siboor.com/siboor-0.2-r1-aug/the-build/initial-startup)

## Quick Summary
### Prerequisites
- This guide focuses on a Windows machine
- Your WiFi signal should be 2.4 GHz or else it would not be detected
- Install a USB Serial CH340 driver to your laptop/PC
- Install an SSH Client
> PuTTY / MobaXterm; I prefer MobaXterm due to file browsing capabilities

**1.)** While powered off and power cable disconnected, connect a USB type C in the backplate of the printer to laptop/PC

**2.)** On your computer, open the Device Manager and identify the port labeled "CH340" under the COM section and get the COM port. (e.g. COM12)

**3.)** Open your SSH Client and create a serial connection:
> *COM Port: "COM port of printer in step 2" <br>
> Baud Rate / Speed: 115200*

**4.)** Proceed and wait for the load screen to appear. If the screen is still blank 5 minutes, try pressing "Enter" or "Space"
> The line "root@flygemini:~#" should appear to verify the connection.

**5.)** Type "**nmtui**" and press "Enter" this opens the network connection manager

**6.)** Navigate and connect to an existing WiFi network *(Check the Siboor V0.2 Guide)*

**7.)** After connecting, exit the network manager and in the serial terminal window, type "**ip a | grep inet**"

**8.)** The terminal reply back IP addresses and retrieve the address: *192.168.XX.XXX*
> Remember the IP address because this will be used to access the printer web page for this specific network.

**9.)** Check the connection by accessing the webpage on a web browser by typing the IP Address from step 9 

**10.)** After verifying that you can access it, shutdown the host using the webpage.

**11.)** You can now disconnect the USB cable and turn on the printer using the power cable
