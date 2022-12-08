# Chapter 2. The Internet

Start: _December 07, 2022_<br />
Finish: _December 07, 2022_

## 1. Introduction

- The internet is a global network of computing devices communicating with each other in some way, whether they're sending emails, downloading files, or sharing websites
- It is an **open network**: any computing device can join as long as they follow the **protocols** which define how each device must communicate with eachother

### To create a global network of computing devices, we need:

- **Wires & wireless**: Physical connections between devices, plus protocols for converting electromagnetic signals into binary data
- **IP**: A protocol that uniquely identify devices using IP addresses and provides a routing strategy to send data to a destination IP address
- **TCP/UDP**: Protocols that can transport packets of data from one device to another and check for errors along the way
- **TLS**: A secure protocol for sending encrypted data so that attackers can't view private information
- **HTTP & DNS**: The protocols powering the World Wide Web, what the browser uses every time you load a webpage

## 2. Computer Networks

**_The internet is the world's largest computer network_**

- A **computer network** is any group of interconnected computing devices capable of sending or receiving data
- A **computing device** isn't just a computer -- it's any device that can run a program, such as a tablet, phone, or smart sensor

### Building a Network

- **Network topology** is the way in which a network is connected
- The larger a network becomes, the more imporant routing stragey is
- Pathfinding algo? large different in data + speed in 20 vs 300 stops

### Types of Networks

- The most common type of networks is the **Local Area Network (LAN)**, a network that covers a limted area like a house or school
- The largest type of network is a **Wide Area Network (WAN)**, a network that extends over a large geographic area and is composed of many, many LANs
  - Oftentimes, the networks in a WAN can only be connected by leasing telecommunications lines from different companies, since no single company owns all the infrastructure across the wide geographic area
- Another type of network is the **Data Center Network (DCN)**, a network used in data centers where data must be exchanged with ver little delay

### Networking Protocols

**_POSSIBLY TO FOLLOW_**

## 3. Bit Rate // Bandwidth // Latency

_All of the computing devices on the Internet are communicating in binary_
_Wired or Wireless, all devices send electromagnetic signals representing 1s and 0s_

### Sending streams of 1s and 0s

- When computers need to internally represent the number 5 (101 in binary)
  - three wires can represnet three bits:
    - Wire 1: On (1)
    - Wire 2: Off (0)
    - Wire 3: On (1)
  - A single wire can be utilzed as long as the time period is agreed upon.
    - Send a single pulse
    - Wait...
    - Sending nothing
    - Wait...
    - Send a single puls
- In an electrical conection such as _Ethernet_, the signal would be a voltage or current.
- In an optical connection such as _fiber-optic cable_, the signal would be the intensity of light.
- The process of turning binary data into a time-based signal is known as _line coding_
  - There are various line coding schemes that can be used based on the needs of the connection

### Bit Rate

-
