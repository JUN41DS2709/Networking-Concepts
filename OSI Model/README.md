# OSI MODEL

<p align="center">
  <img src="images/osi.svg" alt="OSI Diagram" width="700">
</p>

> OSI stands for Open Systems Interconnection. It is a 7-layer conceptual model developed by the International Organization for Standardization (ISO) in 1984.
>
> It was not designed for direct implementation; rather, it serves as a reference model used for troubleshooting, network design, system design, and standardization.

## Why do we need models?

> If network models did not exist, every company would develop its own method of transmitting data. In such a scenario, devices from different vendors might not be able to communicate with each other. The internet as we know it would not exist. Therefore, models are important for standardization and interoperability.

---

## LAYERS OF THE OSI MODEL

> The OSI model consists of 7 layers. Each layer works together with the others for a common goal: the transmission of data.
>
> The 7 layers of the OSI model are as follows:

<p align="center">
  <img src="images/layers.png" alt="layers Diagram" width="700">
</p>

### 7] Application Layer

> The Application Layer is the topmost layer of the OSI model.
>
> It serves as the interface between the user, software applications, and the network.
>
> This layer provides network services such as HTTP, HTTPS, SMTP, SNMP, and FTP to applications.

**Example:**

> Google Chrome
>
> A user wants to visit youtube.com using Google Chrome. The browser acts as an interface that allows the user to communicate over a network and access resources on the internet.
>
> Other examples include YouTube, Gmail, WhatsApp, etc.

**Protocols Used:**

* HTTP
* HTTPS
* FTP
* SMTP
* SNMP

---

### 6] Presentation Layer

> The Presentation Layer comes after the Application Layer.
>
> Its primary responsibility is data translation, compression, encryption, and decryption.
>
> It translates data into a common format so that the receiving application can understand it correctly.
>
> It can also compress data to improve transmission efficiency and encrypt data to enhance security.
>
> On the receiving side, it decrypts and translates the data back into a format that the application can understand.

**Examples:**

* SSL
* TLS
* JPEG
* PNG

---

### 5] Session Layer

> This is the 5th layer of the OSI model.
>
> The Session Layer is responsible for establishing, managing, and terminating communication sessions between devices.
>
> In simple terms, it manages sessions throughout the communication process.

**Real-World Example:**

* Call starts
* Communication takes place
* Call ends

> The Session Layer manages this entire session.

---

### 4] Transport Layer

> The Transport Layer is the 4th layer of the OSI model and is often considered the heart of the OSI model because it sits between the upper and lower layers.
>
> This layer ensures end-to-end communication between the sender and the receiver.
>
> It breaks large amounts of data into smaller segments and assigns sequence numbers to them, helping ensure reliable and orderly delivery.
>
> It also performs flow control and error handling.

**Protocols Used:**

* TCP
* UDP

---

### 3] Network Layer

> The Network Layer receives segments from the Transport Layer and converts them into packets.
>
> It is responsible for logical addressing using IP addresses and routing packets across different networks.
>
> Packets contain information such as source IP address and destination IP address.
>
> This layer determines the best path for packets to travel through the network.

**Key Functions:**

* Logical Addressing
* Routing
* Path Selection

**Examples:**

* IPv4
* IPv6

---

### 2] Data Link Layer

> The Data Link Layer ensures node-to-node delivery within a network.
>
> It receives packets from the Network Layer and converts them into frames.
>
> These frames contain physical addresses known as MAC (Media Access Control) addresses.

**A Frame Contains:**

* Source MAC Address
* Destination MAC Address
* Data
* Error Checking Information (FCS)

> After converting packets into frames, this layer helps deliver data to the correct device within a local network (LAN).
>
> It is responsible for framing, physical addressing, and error detection.

---

### 1] Physical Layer

> The Physical Layer is responsible for transmitting data in the form of raw bits (0s and 1s).
>
> It takes the bit stream from the Data Link Layer and converts it into signals such as electrical signals, light signals, or radio waves.
>
> These signals are transmitted through physical media such as Ethernet cables, optical fiber cables, coaxial cables, and Wi-Fi.

---

## Encapsulation

> Encapsulation is the process of adding headers (and sometimes trailers) to data as it moves down the OSI layers on the sender's side.
>
> Each layer adds its own information before passing the data to the next layer.

---

## Decapsulation

> Decapsulation is the process of removing headers (and trailers) as data moves up the OSI layers on the receiver's side.
>
> This process continues until the receiver obtains the original data sent by the sender.

---

## Protocol Data Units (PDU)

| Layer        | PDU     |
| ------------ | ------- |
| Application  | Data    |
| Presentation | Data    |
| Session      | Data    |
| Transport    | Segment |
| Network      | Packet  |
| Data Link    | Frame   |
| Physical     | Bits    |

---

## Devices and Their Layers

| Device   | Layer                     |
| -------- | ------------------------- |
| Hub      | Physical Layer (Layer 1)  |
| Repeater | Physical Layer (Layer 1)  |
| Switch   | Data Link Layer (Layer 2) |
| Router   | Network Layer (Layer 3)   |
