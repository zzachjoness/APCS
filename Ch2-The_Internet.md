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
- Just like homes need mailing addresses, Internet-connected devices require an IP address to receive messagesJEre
- When a computer sends a message to another computer, it must specify the recipient's IP address and also include its own IP address so that the second computer can reply

  #### IPv4 Addresses

  - IPv4 was the first version used on the Internet
  - IPv4 addreses look like this:

    **74.125.20.113**

  - Each IP address is split into 4 numbers, and each of those numbers can range from 0 to 255:

    **[0-255].[0-255].[0-255].[0-255]**

  - These numbers are stored in binary in the computer:

    **01010101 01010101 0101010101 0101010101**

  - Each number can represnet 2^8^ values, due to the 8 bits, which is also why we often call the "octets"
  - Overall in IPv4 there are 2^32^ possible addresses, that is 4,294,967,296 unique combinations

  #### IPv6 Addresses

  - Back when IPv4 was born, the creators did not anticipate the popularity of the internet, and that more than 2^32^ unique addresses would be required
  - We started running out of IPv4 adddresses in the 1990's, so IPv6 was proposed with a much longer addressing scheme.
  - An IPv6 address looks like this:

    **2001:0db8:0000:0042:0000:8a2e:0370:7334**

  - The letters like d an b shown above are **hexadecimal numbers**, which means that the IPv6 address is much longer than it looks.
  - Hexadecimal numbers are base-16
  - There are 8 hexicideimal numbers, and eah number is 4 digits long.
  - The highest value for each number is _FFFF_

    **FFFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF**

  What is _FFFF_ in decimal?

  | F     | F     | F     | F     |
  | ----- | ----- | ----- | ----- |
  | 16^3^ | 16^2^ | 16^1^ | 16^0^ |
  | 4096  | 256   | 16    | 1     |

  Each F represents 15 in decimal:
  (15 x 4096) + (15 x 256) + (15 x 16) + (15 x 1) = 65,535

  - We can also calculate that based on the binary representation of FFFF
  - Each hexadecimal digit F corresponds to 1111 in binary, so that results in these 16 bits:

    **1111 1111 1111 1111**

  - The highest number that can be represented by _n_ binary digits is 2^n^ - 1
  - 2^16^ -1 = 65,535

  - Each 4-digit hexadecimal number can range between 0 and 65,535
  - There are 8 values, each representing 65,536 unique values
  - In total, each IPv6 address is represented by 128 bits, so there are 2^128^ possible IPv6 address
  - That is 340 undecillion unique addresses:

    **340,282,366,920,938,000,000,000,000,000,000,000,000**

- **Dynamic** IP address can change each day depending on what is assigned by the ISP when you join the network
- Computers that act as servers, like the computers that power Google often have **static** IP addresses

  - This makes it easier for computer to quickly send search requests to the servers

  #### IP Address Hierarchy

  **Consider 24.147.242.217**

  - The first sequence of bits identifies the network and the final bits identify the individual node in the network
  - 24.147 (the first two octets) identifies Comcast network
  - 242.217 (the last two octets) identifies a home computer
  - The Internet Protocol uses this hierarchial addressing scheme to make it easier to route messages form source to destination
  - Once a message arrives at the network, a network router can take care of sending it to the individual node

  #### Subnets

  - Network administrators can break IP addresses into further subnetworks (subnets) as needed

  **Consider 141.213.127.13**

  - 141.213 -> Drexel network
  - 127 -> Engineering department
  - 13 -> Lab computer

  - Adding further levels to the address hierarchy can improve the efficiency of routing within the network

  #### Splitting octets

  - In actuality, IP addresses are often split in the _middle_ of the octets

  **Consider 141.213.127.13 in binary**
  **10001101 11010101 01111111 00001101**

  - All together that translates into 32 bits
  - The first 16 bits could route to all of Drexel
  - The next 2 bits could route to a specific department
  - The final 14 bits could route to individual computers

## 4. Routing

**_The Internet Protocol (IP) describes the strcuture of the packets that are sent on the internet_**

- **Packets** are the smaller bits in which messages are split up in when being sent on the internet
- Each IP packet contains both a header (20 or 24 bytes long) and data (variable length)
  - The header includes the IP address of the source and destination, plus other fields that help to route the packet
  - The data is the content, i.e. strings of letters or part of a webpage

### Step 1: Send packet to router

- Computers send the first packet to the nearest router

### Step 2: Router receives packet

- Router looks @ the IP addresses

### Step 3: Router forwards packet

- The router has multiple paths it could send a packet along
- The router decides the path by utilzing its **forwarding table**
- Router locates the most specific row and chooses that address

### Step 4: Final router forwards message

- Router can send message to destination IP address which could be a PC or server

- When we're trying to make sure a system is **fault tolerant** we look for single points of failure and find ways to add **redundancy** at those points

## 5. Transporting Packets

### Problems with Packets

- A computer may send **multiple messages** to a destination and the destination needs to identify which packets belon to which message
- Packets can arrive **out of order**, this can heppen especially if two packets follow different paths to the destination
- Packets can be **corrupted**, meaning the received data no longer matches the originally sent data
- Packets can be **lost** due to problems in the physical layer or in routers' forwarding tables
  - If one packet of a message is lost it may be impossible to put the message back together in a way that makes sense
- Similarly, packets might be **duplicated** due to accidental retransmission of the same packet

### User Datagram Protocol (UDP)

- The **User Datagram Protocol (UDP)** is a lightweight data transport protocol that works on top of IP
- UPD provides a mechanism to detect corrupt data in packets, but does not attempt to solve other problems that arise, such as lost or out of order packets
- UDP is sometimes known as the **_Unreliable Data Protocol_**
- When sending packets using UDP over IP, the data portion for each IP packet is formatted as a UDP segment
- Each UPD segment contains an 8-byte header and variable length data

  #### Port Numbers

  - The frist four bytes of the UDP header store the port numbers for the source and destination
  - A networked device can reeive messages on different virtual ports
  - The different ports help distinguish different types of network traffic

  #### Segment Length

  - The next two bytes of the UDP header store the length (in bytes) of the segment

  #### Checksum

  - The final two bytes of the UDP header is the checksum, a field that's used by the sender and receiver to check for data corruption
  - Before sending off the segment, the sender:
    1. Computes the checksum based on the data in the segment
    2. Stores the computed checksum in the field
  - Upon receiving the segment, the recipient:
    1. Computes the checksum based on the received segment
    2. Compares the checksums to eachother; if the checksums are not equal, it knows the data was corrupted
  - When the recipient discovers that two checksums are different, it understands that the data has been corrupted.
  - Unfortunately, the recipient cannot use the computed checksum to reconstruct the original data, so it will likely discard the packet entirely

### Transmission Control Protocol (TCP)

- The **Transmission Control Protocol (TCP)** is a transport protocol that is used on top of IP to ensure reliable transmission of packets
- TCP includes mechanisms to solve many of the problems that arise from packet-based messaging such as lost, out of order, duplicate, and correpted packets
- Since TCP is the protocol used most commonly on top of IP, the Internet protocol stack is somtimes referred to as **TCP/IP**

  #### Packet Format

  - When sending packets using TCP/IP, the data portion of each IP packet is formatted as a **TCP segment**

  ![TCP Segment!](/images/TCP_diagram.svg "TCP SEGMENT")

  - Each TCP segment contains a header and data
  - The TCP header contains many more fields than the UDP header and can range in size from 20 to 60 bytes

  #### Transmitting a packet with TCP/IP

  ##### Step 1: Establish connection

  - When two computers want to send data to each other over TCP, they first need to esablish a connection using a **three-way handshake**

  ![Three-way handshake!](/images/TWH.svg "Three-way handshake")

  #### Step 2: Send Packets of Data

  - When a packet of data is sent over TCP, the recipient must always acknowledge what they have received
  - The acknowledgement number is increased by the length of the received data, which is part of the TCP header
  - The sequence and acknowledgement numbers help the computers keep track of which data has been successfully received, lost, and/or sent twice

  #### Step 3: Close the Connection

  - Either computer can close the connection

  ![FIN!](/images/Close_Connection.svg "Close Connection")

  ### Detecting Lost Packets

  - TCP conections can detect lost packets using a timeout
  - If the timer runs out and the ACK is not received, the packet is sent again

  ### Handling Out of Order Packets

  - ACK & SEQ numbers are used to detect out of order packets
  - SEQ numbers are used to deal with out of order packets and to reassemble the data in correct order
