
Part A: Network Devices Research


1. Router
Purpose:
A router connects different networks and allows devices to access the internet

How it Works:
The router receives data from one network and forwards it to the correct destination using IP addresses.

Real-World Usage:
Routers are commonly used in homes, schools, offices, and businesses to provide internet access to multiple devices.

2. Switch
Purpose:
A switch connects multiple devices within the same network.

How it Works:
It uses MAC addresses to send data only to the intended device, making communication faster and more efficient.

Real-World Usage:
Switches are used in offices, schools, and computer labs where many computers need to communicate on the same network.

3. Hub
Purpose:
A hub connects multiple devices in a network.

How it Works:
Unlike a switch, a hub sends incoming data to all connected devices, regardless of the destination.

Real-World Usage:
Hubs were used in older networks but are now mostly replaced by switches because switches are more efficient.

4. Access Point
Purpose:
An access point provides wireless connectivity to devices.

How it Works:
It connects to a wired network and broadcasts a Wi-Fi signal, allowing wireless devices to join the network.

Real-World Usage:
Access points are commonly found in schools, offices, hotels, and public places to extend Wi-Fi coverage.

5. Firewall
Purpose:
A firewall protects a network from unauthorized access and cyber threats.

How it Works:
It monitors incoming and outgoing traffic and blocks suspicious or harmful data based on security rules.

Real-World Usage:
Firewalls are used in homes, businesses, and organizations to protect computers and networks from attacks.

6. Modem
Purpose:
A modem connects a home or office network to an Internet Service Provider (ISP).

How it Works:
It converts digital data from devices into signals that can travel through telephone, cable, or fiber lines.

Real-World Usage:
Modems are used in homes and offices to provide internet connectivity.


Part B: IP Address Classification

IP Address
Type

192.168.1.10

Private
Belongs to the private range 192.168.0.0 – 192.168.255.255.
10.0.0.5

Private
Belongs to the private range 10.0.0.0 – 10.255.255.255.
172.16.5.20

Private
Belongs to the private range 172.16.0.0 – 172.31.255.255.
8.8.8.8

Public
Public IP address used by Google's DNS service.
1.1.1.1

Public
Public IP address used by Cloudflare's DNS service.
192.168.100.1

Private
Belongs to the private range 192.168.0.0 – 192.168.255.255.

Why They Belong to These Categories?
 ans )=Private IP addresses are reserved for use within local networks and cannot be accessed directly from the internet. Public IP addresses are globally unique and can be accessed over the internet.

Part C: Understanding Your Network
IPv4 Address
Example: 192.168.1.5
Default Gateway
Example: 192.168.1.1
DNS Server
Example: 8.8.8.8



1. Which IP Range Does Your Device Belong To?
My device belongs to the 192.168.1.0/24 private IP range because its IPv4 address starts with 192.168.1.

2. Is It Public or Private?
It is a Private IP Address because it belongs to the reserved private IP range used inside local networks.

3. What Role Does Your Router Play in Your Network?
The router acts as a gateway between my local network and the internet. It assigns IP addresses to devices, manages network traffic, and ensures that data reaches the correct destination.

4. What Would Happen If the DNS Server Stopped Working?
If the DNS server stopped working, websites could not be accessed using their names (such as google.com). Internet access might still work through IP addresses, but browsing websites would become difficult because domain names would not be translated into IP addresses.

Part D: Network Communication Flow
Diagram:
Your Device → Router → DNS Server → Google Server → Response Back to Device


1. Your Device When you type www.google.com⁠� in a web browser, your computer or mobile device sends a request to access the website.

2. Router The router receives the request and forwards it to the internet through your Internet Service Provider (ISP).

3. DNS Server The DNS server converts the domain name www.google.com into an IP address that computers can understand.

4. Google Server Using the IP address, the request reaches Google's server. The server processes the request and prepares the webpage data.

5. Response Back to Device The Google server sends the webpage data back through the internet and router to your device, where the webpage is displayed.


Part E: Practical Command Exercise
Answers

1. What IP address did DNS return for Google?
Example:

142.250.193.78

2. Was the ping successful?
Yes, the ping was successful if replies were received from Google's server.
Example:

Reply from 142.250.193.78: bytes=32 time=25ms TTL=117


3. Why is DNS important before communication begins?
DNS is important because it converts website names such as google.com into IP addresses. Without DNS, devices would not know the server's address and communication could not begin.


Commands Used
Windows

ipconfig /all
nslookup google.com
ping google.com


Linux
Bash
ip addr
nslookup google.com
ping google.com