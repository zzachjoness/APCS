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
- In an electrical conection such as **Ethernet**, the signal would be a voltage or current.
- In an optical connection such as **fiber-optic cable**, the signal would be the intensity of light.
- The process of turning binary data into a time-based signal is known as _line coding_
  - There are various line coding schemes that can be used based on the needs of the connection

### Bit Rate

- Network connections can send bits very fast; we measure that speed using the **bit rate**, the nmber of bits of data that are sent per second
- The earliest Internet connections were just 75 bits per second (bps)
- In the year 2022, connections are often measured in Mbps

### Bandwidth

- The term **bandwidth** describes the maxiumum bit rate of a system
- If a network connection has a bandwidth of 100 Mbps, this means it cannot transfer more than 100 megabits per second
- The term _broadband Internet_ refers to a connection with a minimum bandwidth of 256 Kbps, enough speed to check emails and browse the web

### Latency

- The term **latency** is used to descrube how late bits arrive, i.e. the time between the sending of a data message and the receiving of that meassage, measured in milliseconds
- Latency is also reffered to as the "ping rate"
- Most often we measure the "round-trip" latency of a request
  - A request is send to the Google server which takes 30ms to receive
  - 40ms later we recieve notice that Google recieved the data
  - The total round-trip latency is 70ms for this transaction
- Latency depends on a number of physical factors
  - Type of connection between parites
  - Distance between connections
  - Network congestion
- The major limiting factor of latency is the speed of light, which nothing can move faster than 1ft/ns

### Internet Speed

- Speed is a combination of bandwidth and latency
- Computers split up messages into packets, and they cannot send another message until the frist packet is received

### IP Address

- The **Internet Protocol (IP)** is one of the core protocols in the layers of the Internet, it is used in all Internet communication to handle both addressing and routing
- The protocol describes the use of **IP addresses** to uniquely identify Internet-connected devices
- Just like homes need mailing addresses, Internet-connected devices require an IP address to receive messages
- When a computer sends a message to another computer, it must specify the recipient's IP address and also include its own IP address so that the second computer can reply

  #### IPv4 Addresses

  - IPv4 was the first version used on the Internet
  - IPv4 addreses look like this:

    > **74.125.20.113**

  - Each IP address is split into 4 numbers, and each of those numbers can range from 0 to 255:

    > **[0-255].[0-255].[0-255].[0-255]**
