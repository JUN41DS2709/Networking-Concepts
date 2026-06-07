# TCP/IP MODEL

<p align="center">
  <img src="images/tcpip.png" alt="TCP/IP Diagram" width="700">
</p>


TCP/IP Model is the foundational and most fundamental networking model. It was developed by the U.S. Department of Defense (DARPA), and work on the TCP/IP model started in the early 1970s.

The TCP/IP model contains a set of rules and protocols that ensure reliable delivery of data across a network while protecting its integrity.

TCP/IP is a four-layered model which includes:

1. Application Layer
2. Transport Layer
3. Internet Layer
4. Network Access Layer

---

# 1] APPLICATION LAYER

It serves as the direct interface between the user/software and the network.

It provides network services to applications so that users can interact, provide data input, and communicate over the network.

### Example:

WhatsApp is an application used for communication with our family, friends, or anyone over the Internet.

We type a message to our friend using the WhatsApp UI, and the message gets transferred with the help of network services used by WhatsApp.

### Common Protocols:

* HTTP / HTTPS (Web Browsing)
* FTP (File Transfer)
* SMTP (Email)
* DNS (Domain Name Resolution)

---

# 2] TRANSPORT LAYER

The Transport Layer ensures end-to-end delivery of data.

It helps in preventing errors and managing the flow control of data by dividing the data into smaller pieces called **segments** and assigning sequence numbers for efficient and reliable delivery (in TCP).

This layer is also responsible for:

* Segmentation
* Reassembly
* Flow Control
* Error Detection
* End-to-End Communication

### Protocols Used:

* TCP (Transmission Control Protocol)
* UDP (User Datagram Protocol)

### Examples:

* TCP → Web Browsing, File Transfer, Email
* UDP → Online Gaming, Video Streaming, VoIP Calls

---

# 3] INTERNET LAYER

This layer acts as the postman of the network.

It converts segments into packets, which contain:

* Source IP Address
* Destination IP Address
* Data

This layer handles logical addressing (IP Addressing).

It is responsible for routing data across networks and determining the best path for data transmission.

### Functions:

* Logical Addressing
* Packet Forwarding
* Routing
* Path Determination

### Protocols Used:

* IPv4
* IPv6
* ICMP

### Example:

When you send a message from Mumbai to Delhi, the Internet Layer helps determine the best route for the packet to reach its destination.

---

# 4] NETWORK ACCESS LAYER

This layer handles data transmission over a physical medium.

It transmits data as raw bits (0s and 1s).

It works by converting data into physical signals such as:

* Electrical Signals
* Light Signals
* Radio Waves

This layer is responsible for:

* Framing
* MAC Addressing
* Physical Transmission of Data

### Examples of Technologies and Media:

* Ethernet
* Wi-Fi
* Coaxial Cable
* Optical Fiber
* Twisted Pair Cable

---

# DATA ENCAPSULATION PROCESS

As data moves down the TCP/IP model, its format changes:

Application Layer
↓
Data

Transport Layer
↓
Segment

Internet Layer
↓
Packet

Network Access Layer
↓
Frame

Physical Medium
↓
Bits (0s and 1s)

---

# QUICK SUMMARY

| Layer                | Main Responsibility                            | Data Unit |
| -------------------- | ---------------------------------------------- | --------- |
| Application Layer    | Provides network services to applications      | Data      |
| Transport Layer      | End-to-end delivery, reliability, flow control | Segment   |
| Internet Layer       | IP addressing and routing                      | Packet    |
| Network Access Layer | MAC addressing and physical transmission       | Frame     |

---

# REAL-WORLD EXAMPLE

You send a WhatsApp message:

1. Application Layer → Creates the message.
2. Transport Layer → Breaks the message into segments.
3. Internet Layer → Adds source and destination IP addresses and creates packets.
4. Network Access Layer → Creates frames and sends them as bits through Wi-Fi, Ethernet, or Fiber.
5. The receiver gets the message through the reverse process (Decapsulation).



