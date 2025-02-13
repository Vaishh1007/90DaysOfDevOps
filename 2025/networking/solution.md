***How does internet works?***
-It is a web of cables(optical fibres) where data is transfer from one location to anothor.
-a hierarchy of networks is divided into tiers:


***Tier 1: The Backbone of the Internet***

The top level of the internet. These are the biggest networks in the world.

Huge companies that own and operate massive infrastructure, like undersea cables and data centers (e.g., Level 3, NTT Communications, and Telia).

Tier 1 networks connect directly to one another without paying anyone else. They exchange traffic freely (this is called "peering"). They are the reason global communication is possible.


***Tier 2: The Middlemen***

Regional or national networks that connect to Tier 1 networks.

They pay Tier 1 providers for access to the global internet.

Tier 2 providers act as bridges, connecting local ISPs or businesses to the global internet. They might also peer with other Tier 2 networks to reduce costs.


***Tier 3: Local Providers***

Smaller networks that provide internet to homes and businesses.

Local ISPs, like your neighborhood internet provider or small cable companies.

Tier 3 providers pay Tier 2 (or sometimes directly Tier 1) providers to carry internet traffic. They bring the internet directly to your door.


***Example of the Internet in Action:***
You type a website address on your computer.

Your Tier 3 provider sends the request to a Tier 2 provider.

The Tier 2 provider forwards it to a Tier 1 network to reach the website's server, possibly across continents.

The server sends back the data through the same chain, and the website appears on your screen!


In short:

Tier 1: The global highways.

Tier 2: The regional roads.

Tier 3: The local streets.



***What Is Network Infrastructure and Why Is It Important?***


***OSI Model***
Helps standardize network communication.

Makes troubleshooting easier.

Provides a common language for networking professionals.


***Seven layers of OSI Model :***

Physical Layer: Handles the physical transmission of data (cables, signals).

Example: Ethernet, Wi-Fi, mobile networks.
Data Link Layer: Manages data transfer between devices on the same network (MAC addresses).

Example: Your phone's network card sends frames to your home Wi-Fi router.
Network Layer: Determines the best path for data (IP addresses, routing).

Example: The data is routed through the internet using protocols like IP.
Transport Layer: Ensures reliable data delivery (TCP/UDP, error checking

Example: TCP ensures each chunk of your message reaches the recipient's device without errors.
Session Layer: Manages and controls communication sessions between devices.

Example: Keeps the connection active while sending/receiving the message.
Presentation Layer: Formats, encrypts, or compresses data for the application layer.

Example: WhatsApp encrypts the text, images, or videos being sent.
Application Layer: Enables user interaction with the network (browsers, email apps).

Example: You type a message, hit send, and the app displays "Message Sent" when the delivery is complete.
Overview of OSI model & HTTP protocol | by Arshad Suraj | Medium


TCP/IP Model
TCP/IP is the backbone of the internet, allowing different devices to communicate seamlessly!
Application Layer:

Combines OSI's top three layers (Application, Presentation, and Session

Provides services like web browsing, email, and file transfer (e.g., HTTP, FTP, SMTP).

Transport Layer:

Handles end-to-end communication and ensures reliable data delivery using protocols like TCP (reliable) or UDP (faster but less reliable).
Internet Layer:

Responsible for routing data across networks using IP addresses (e.g., IPv4, IPv6)

Determining the best path for packets.

Network Access Layer (or Link Layer): -

Deals with physical hardware, such as network interfaces, and manages how data is sent over the physical network (e.g., Ethernet, Wi-Fi).

Example:

You type website’s url into your browser.

The browser establishes a connection with the web server.

Data packets are routed through the internet from your computer to the web server's IP address.

The packets are sent across the physical network (like Wi-Fi or Ethernet) to the next device (e.g., router).

TCP/IP Model Explained: A Guide to Computer Networking



***Protocols***
A protocol is a set of rules that defines how data is transmitted and received over a network.



1. Application Layer Protocols

Enable communication for specific tasks or applications:

HTTP/HTTPS: Web browsing (secure with HTTPS).

FTP: File transfer between computers.

SMTP: Sending emails.

POP3/IMAP: Receiving emails.

DNS: Resolving domain names to IP addresses.

SSH: Secure remote login to devices.



2. Transport Layer Protocols

Ensure proper data delivery:

TCP (Transmission Control Protocol): Reliable, connection-oriented communication (e.g., web browsing, email).

UDP (User Datagram Protocol): Fast, connectionless communication (e.g., video streaming, gaming).




3. Internet Layer Protocols

Handle routing and addressing:

IP (Internet Protocol): Moves packets across networks (IPv4, IPv6).

ICMP: Sends error messages (e.g., when a server is unreachable).

ARP: Resolves IP addresses to MAC addresses.




4. Network Access Layer Protocols

Manage data transmission over physical media:

Ethernet: Local area network communication.

Wi-Fi (IEEE 802.11): Wireless communication.

PPP (Point-to-Point Protocol): Direct connections between devices.




***Important Protocols and Ports required for DevOps***

HTTP/HTTPS

Port: 80 (HTTP), 443 (HTTPS)

Use: Accessing web services, APIs, and websites.

SSH (Secure Shell)

Port: 22

Use: Secure remote access to servers for configuration, troubleshooting, and deployment.

DNS (Domain Name System)

Port: 53

Use: Resolving domain names to IP addresses, vital for accessing services by name.

SMTP (Simple Mail Transfer Protocol)

Port: 25, 587 (secure mail submission), 465 (SMTPS)

Use: Sending emails, often used for notifications in CI/CD pipelines.

POP3/IMAP

Port: 110 (POP3), 143 (IMAP), 993 (IMAPS), 995 (POP3S)

Use: Receiving email messages (e.g., for monitoring alerts).

FTP/SFTP

Port: 21 (FTP), 22 (SFTP)

Use: Transferring files between systems.

MySQL

Port: 3306

Use: Access to MySQL databases.




***MAC Addresses***

A MAC (Media Access Control) Address is a unique identifier assigned to a device's network interface card (NIC).

It’s like a permanent "serial number" for hardware on a network.

It identifies a device on a local network (like Ethernet or Wi-Fi).

Used for communication between devices on the same network.

A MAC address is a 48-bit (6-byte) number, typically written in hexadecimal format.

Example: 00:1A:2B:3C:4D:5E or 00-1A-2B-3C-4D-5E.



***What is MAC Address and How to find it? -***


Types of MAC Addresses


Unicast MAC Address:

Unique to one device. Used for one-to-one communication.

Example: Sending data to a specific laptop.


Multicast MAC Address:

Shared by a group of devices. Used for one-to-many communication.

Example: Streaming video to multiple users on a network.



Broadcast MAC Address:

FF:FF:FF:FF:FF:FF is used to communicate with all devices on a network.
Routers and Switches
Router: connects networks (like your home to the internet).
Switch: connects devices within the same network (like computers and printers).


***Key Difference Between Router and Switch***
Feature	Router	Switch
Purpose	Connects different networks (e.g., LAN to internet).	Connects devices within the same network (LAN).
Addressing	Uses IP addresses (Layer 3).	Uses MAC addresses (Layer 2).
Example Use	Your Wi-Fi router connects your devices to the internet.	A switch connects devices like laptops and printers within your office.
Difference between Switch and Router - javatpoint

For Example,

In a Home Network:

Router: Connects your entire home network to the internet.

Switch: Connects multiple devices like TVs, laptops, and printers so they can talk to each other locally.




***How to Create and Configure Security Groups in AWS***
Step 1: Log in to AWS Management Console

Step 2: Navigate to Security Groups

Step 3: Define Security Group Details

Step 4: Configure Inbound Rules

Step 5: Configure Outbound Rules

Step 6: Review and Create

Step 7: Associate Security Group with an EC2 Instance





***Essential networking commands for devops***

ping – Checks connectivity to a host.

traceroute (Linux) / tracert (Windows) – Shows the path packets take to a destination.

nslookup – Queries DNS records.

dig – Retrieves DNS records in detail (Linux/macOS).

host – Resolves domain names to IP addresses.

ifconfig (deprecated) / ip a (Linux) / ipconfig (Windows) – Displays network interface information.

ip route – Shows routing table



***Conclusion***
The internet works as a global web of interconnected networks, structured into tiers (Tier 1, 2, and 3) that facilitate data transfer from one location to another. The OSI and TCP/IP models standardize communication processes, while protocols and hardware like routers, switches, and MAC addresses enable seamless and efficient data flow. These concepts are fundamental to understanding how devices interact, networks are managed, and services like web browsing, email, and cloud-based applications operate in real-world scenarios.
