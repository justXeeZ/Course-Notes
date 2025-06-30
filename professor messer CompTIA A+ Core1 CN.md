# Comptia A+ Core 1 Course Notes

## 1- Laptob Hardware

### laptop batteries
- Lithium-ion (Li-ion) and Lithium-Ion polymer have no "memory effect" and charging battery doesn't deminish capacity

### laptop keyboard 
- they are mostly easy to replace as they connect to the laptop by a few screws and a ribbon cable
- be careful! the keycaps are very fragile

### laptop memory
- small Outline Dual In-Line Memory Module (SO-DIMM)
- often easy to install
- sometimes they are soldered to the board (that's sad)

### laptop storage
- installing drives is often easy
- Hard Disk Drive (HDD) Magnetic disks, the traditional spinning drive platters, 2.5 form factors for laptops and 3.5 for desktops
- Solid State Dirve (SSD), no moving parts so silent, fast, and more reliable, always 2.5 inch form factor
- Non-Volatile Memory Express (NVMe) uses an M.2 interface and utilizes the PCI-e so they are much faster
- SSDs sometimes use an M.2 interface
- you can image/ clone dirves using commercial or open source software, sometimes manufacturers make this sofware

### 802.11 wireless and bluetooth
- they use PCI interfaces
- the are wireless netowrks _duh_
- 802.11 or wi-fi (i know, surprising) is a Local Area Network (LAN)
- Bluetooth has a shorter range than wi-fi that's why it is a Personal Area Network (PAN)
- these cards use antennas that wrap in the screen to have better signal

### biometrics
- utilizes software and hardware
- finger print, facial recognition

### Near-Field Communication (NFC)
- short distance netword (4cm or less) used for small data transfer or authentication without typing a password

### camera/ webcam
- usually includes both audio and video

### notes:
```
you can be very familiar with a specific manufacturer
devices from the same manufacturer are often built similarly
```

## 2- Connecting mobile devices

### connection
- Universal Serial Bus (USB) like Micro, Mini B, Type A (most popular), Type C (the future, and thunderbolt) USBs
- apple proprietary cable is called lightning
- lightning and type C can be inserted in any orientaion

### wireless connection
- like bluetooth, wifi, NFC (which can be used as an access token or an "ID card")
- mobiles can be used as internet routers via the "Hot Spot" feature

```
sometimes mobiles are used for synchorization, backup and identification
```

## 3- Mobile device accessories

### stylus
- more percise, work with pressure and can have programmable buttons, just douple check the compatibility

### headsets
- wireless: connect via bluetooth

- wired 
	- USB connections (common in laptops)
	- 3.5mm Tip-Ring-Ring-Sleeve (TRRS) connector
	- Analog audio jack 
	- Lightning port in iPhone

### speakers
- they are battery powered in mobiles, often stereo in more modern phones

### camera/ webcam
- internal (in laptops or phones) or external (in desktops)

### docking stations
- often use a specified interface to connect the laptop
- they use an external keyboard, mouse
- they add aditional functionality while avoiding cable issues

### port replicator
- adds more connectors like USB, Display, Ethernet
- I ususally call it a USB hub

### trackpad
- replaces the mouse and common in laptops
- they add aditional touch gestures and functionality

### drawing pad
- similar to a trackpad but comes with a stylus for aditional percision

## 4- Mobile device netwroks

### cellular networks
- they use antenna coverage and seperate land into "cells" and communicates with certain frequencies
- they provide data and voice connection, you can turn both of them off using the airplane mode
- 3G introduced new functionality as GPS, Mobile Televesion, Video conferencing, etc...
- 4G Long Term Evolution (LTE) supports standard download rate of 150 Mbit/s, there is LTE Advanced which supports up to 300 Mbit/s
- 5G up to 10 Gbit/s with slower speeds from 100-900 Mbit/s

### Wi-Fi
- again, the 802.11 network
- support voice communications (good in absence of cellular networks)

### hotspot
- your device connects to a cellular network like 5G, and then other devices connect to it via Wi-Fi

### Subscriber Identity Module (SIM)
- it is a unique identifier for cellular devices
- it is often a tiny physical card
- has small storage to carry contacts and messages
- embedded SIM (eSIM) in newer devices cannot be removed (as the name suggests), changes the number via software

### bluetooth
- it connects between different devices via pairing process for one time manually then it happens automatically

### Global Positioning System (GPS)
- needs at least 4 satellites and determines location based on Longitude, Latitude, Altitude
- GPS isn't the only way to determine your locate, Wi-Fi and cellular towers are used too (You are not safe!)

## 5- Mobile Device Mangament

### Mobile Device Management (MDM)
- the company manages devices functionality and sets policies on hings like the camera, apps, data etc...
- the company can use the entire device or just a partition of the device

### Bring Your Own Device (BYOD)
- BYOD is relatively harder to secure as the employee owns the device and uses it personally 

### Company Owned Personally Enabled (COPE)
- the company buys the device and has full control over the phone
- there is stronger policies concerning the safety of the data in case if the device is lost than BYOD
- Choose Your Own Device (CYOD), similar to COPE but the user can choose the device

### MDM policy enforcement
- the corporate ususally configures the email so that the user doesn't have to configure any thing
- they usually require two-factor authenitcaion types like biometrics or psuedo-random authentication apps
- they also allow or restrict apps installaions and prevent unauthorized app usage

### mobile device synchorization
- it is important for backup and recovery, usually for calendars, contacts etc...
- if the cellular data is not monitored, it will hurt the company financially 

### business applications
- like mail, cloud storage, authentication and so on
- they are often built in to the mobile device

## 6- introduction to IP

### a series of moving vans
- the ethernet cable is the road, the truck is the Internet Protocol (IP) which contains boxes of (TCP) and (UDP), these boxes contains the information

### TCP and UDP
- they are both encapsulated inside the IP, they are both made to move data from one place to another
- usually refered to as "OSI Layer 4" (and yes, idk what that is)
- they allow us to send and recieve to multiple devices simoultanously which is called (Multiplexing)

### Transimition Control Protocol (TCP)
- there is a formal connection setup and close which means that when the reciever recieves the data, his device sends back a TCP Acknowledgment confirming that the data was sent successfully
- it is a "Reliable delivery" so it can recover from errors by sending an acknowledgment to the sender saying that there was an error sending the data so that the sender can send the data again
- it has "Flow Control" which means that the receiver can manage how much data is sent

### User Datagram Protocol (UDP)
- it is connectionless so no formal open or close to the connection
- it is an "Unreliable delivery" so also no error recovery and no reordering data or retransmitissions
- also no flow control so the sender is the one who determines the amount of data transmitted

### why would you ever use UDP
- for real-time communication as it has the least amount of over-head and there is no need to worry about data that hasn't been sent
- there are some connectionless protocols like Dynamic Host Configuration Protocol (DHCP) and Trivial File Transfer Protocol (TFTP) which are usually used with UDP
- the application might handle the lost data and resend them

### communication using TCP
- there are connection-oriented protocols that prefer a "return receipt" aka the TCP Ack like HyperText Transfer Protocol Secure (HTTP, HTTPS) and Secure Shell (SSH)
- the application doesn't worry about missing data as TCP handles all the communication overhead, the app has one job, the app does its one job

### port numbers
- every server and client has an IP Address
- applications uses port numbers which are an "extension" of that IP address
- IPv4 sockets has 2 information bundles that are important:
	- Server IP Address, protocol (TCP or UDP), server application port number
	- Client IP Address, protocol, client port number
- there are 2 types of port numbers
	- Non-ephermal ports or Permanent port numbers, usually on a server or a service from 0 to 1,023
	- Ephermal ports or temporary port numbers determined in real time by the client from 1,024 to 65,535
- so TCP and UDP ports can be from 0 to 65,535
- note that the port numbers are just a number used for communication no security
- note that TCP port 80 (tcp/80) is different from UDP port 80 (udp/80)

### ports on the network
- we have three servers: web server (tcp/80), Voice Over IP server (VoIP) (udp/5004), Email sever (tcp/143)
- the data sent from the client to the server respectivly is:
	- [ Ethernet Header | IP | TCP |  HTTP data | Ethernet Trailer ]
	- [ Ethernet Header | IP | UDP |  VoIP data | Ethernet Trailer ]
	- [ Ethernet Header | IP | TCP | Email data | Ethernet Trailer ]
- we said earlier that we can send and recieve a lot of data simoultinasouly thanks to multiplexing
- pay attention to the ports (as we said server ports are usually Non-ephermal, so the ports that usually change are the client ports)
	- [ source IPa = 10.0.0.1 | TCP Source Port = 3000 | HTTP Data ]
	- [  Dest IPa = 10.0.0.2  |   TCP Dest Port = 80   | HTTP Data ]

## 7- common ports

### port numbers
- there are some well known port numbers that the client and server need to match
- they are important for firewall rules as the firewall uses port-based security

### File Transfer Protocol (FTP)
- tcp/20 (active mode data or active file transfer)
- tcp/21 (control or administraion)
- there is usually some type of authentication using a username and password
- you can list, add, delete files

### Secure Shell (SSH)
- tcp/22 (provides encrypted communication link)
- used to connect to a remote device and have a console access

### Telnet
- tcp/23 (doesn't provide any form of encryption, and it is old so SSH is preferable)

### Simple Mail Transfer Protocol (SMTP)
- tcp/25 (server to server email transfer)
- also can be used to send mail from a device to a mail server and is commonly configured on mobile devices
- other protocols are used for clients to receive emails as IMAP and POP3

### Domain Name System (DNS)
- udp/53 (converts names to IP addresses)
- it converts host names to IPAs like : dns.google.com = 8.8.8.8

### Dynamic Host Configuration Protocol (DHCP)
- udp/67, udp/68 (automates configuration of IPAs, Subnet mask and other options)
- it requires a DHCP server, appliance or integrated into a Small Office Home Office router
- IPAs are assigned in real time from a pool and each system is given a lease and must renew at set intervals
- you can configure the DHCP to reserve a specific IPA to a certain device each time that device starts up

### Hyper Text Transfer Protocol Secure (HTTP) or (HTTPS)
- tcp/80 (HTTP used for web server communication)
- tcp/443 (HTTPS like HTTP but with encryption)
- used for communication in the browser and by othe applications

### POP3 / IMAP
- tcp/110 (Post Office Protocol v3 (POP3) offers basic mail transfer functionality)
- tcp/143 (Internet Message Access Protocol v4 (IMAP4) includes management of email inbox from multiple clients and supports synchorization)

### Server Message Block (SMB)
- also called Common Internet File System (CIFS) and used for file sharing and printer sharing
- older windows devices uses an aditional protocol inside TCP/IP called NetBIOS and works over:
	- udp/137 (NetBIOS same services "nbname" which is similar to DNS)
	- tcp/139 (NetBIOS session service "nbsession" which is used to setup sessions to transfer files)
- tcp/445 (modern windwos devices use direct SMB communication over TCP without the need to NetBIOS "NetBIOS-less")

### LDAP / LDAPS
- tcp/389 (Lightwaight Directory Access Protocol Secure (LDAP), (LDAPS) used for storing and retrieving information in a network directory)
- commonly used in Microsoft Active Directory
- the analogy below shows a simple representation

| | organization | |
| ---------- | -------- | ----------- |
| Production |  Support | Engineering |
|    Jack    | tech docs (database)| sam |
|    Dani    | meowchil |    hamood   |

### Remote Desktop Protocol
- tcp/3389 (used for sharing a desktop from a remote location)

### Quick overview of common ports
|Port|Service|
|---|---|
|tcp/20 |FTP Active Mode|
|tcp/21 |FTP Control|
|tcp/22 |SSH|
|tcp/23 |Telnet|
|tcp/25 |SMTP|
|udp/53 |DNS|
|udp/67 |DHCP|
|udp/68 |DHCP|
|tcp/80 |HTTP|
|tcp/443|HTTPS|
|tcp/110|POP3|
|tcp/143|IMAP4|
|udp/137|NetBIOS (nbname)|
|tcp/139|NetBIOS (nbsession)|
|tcp/445|NetBIOS-less|
|tcp/389|LDAP/LDAPS|
|tcp/3389|RDP|

## 8- Wireless Netwrok Technologies

### Wireless technologies
- the Institute of Electriacl and Electronic Engineers (IEEE) makes the 802.11 comitee (Wi-Fi) that everyone follows
- 802.11ac is Wifi 5, 802.11ax is Wifi 6 and 802.11be is Wifi 7 and so on in the future

### 802.11 technologies
- there are many frequencies like the 2.4GHz range, 5GHz range and 6GHz range, these ranges containes channels or groups of frequencies numbered by the IEE
- the bandwidth is the amount of frequency in use like 20MHz, 40MHz, 80MHz, 160MHz, etc...

### bluetooth
- uses the 2.4GHz range and it this frequencey is sometimes refered to as unlicenced ISM (Industrial, Scientific and Medical) band, which means that these devices doesn't require any specialized licence to use, them same as 802.11
- its short range reaches a maximum about 10 meters for most consumer devices

### Radio-Frequency Identification (RFID)
- it is in access badges or cards, pet identification, anything that needs to be tracked
- they are usually sitting idle with no power but when exposed to radio frequency, its energy is enough to power the tag (RFID)
- some tags are powered by batteries

### Near Field Communicaion (NFC)
- it builds on the RFID which is mostly one way to be a two way wireless communication
- used heavily in payment systems
- NFC can help in bluetooth pairing
