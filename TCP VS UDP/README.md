# TCP and UDP

## TCP

**TCP** stands for **Transmission Control Protocol**.

It is a **connection-oriented protocol** used for reliable and error-free transmission of data between the sender and the receiver.

TCP uses a **three-way handshake** to securely establish a connection and ensure that data is transmitted in the correct order without errors.

### TCP Three-Way Handshake

The connection establishment process consists of three steps:

1. **SYN** – The sender sends a request to initiate a connection.
2. **SYN-ACK** – The receiver acknowledges the request and responds with its own synchronization request.
3. **ACK** – The sender acknowledges the receiver's response, and the connection is established.

After these steps, data can be exchanged between both devices.

### Connection Termination

When closing the connection, TCP follows a termination process:

1. **FIN** – The sender requests to close the connection.
2. **FIN-ACK** – The receiver acknowledges the request to terminate the connection.
3. **ACK** – The sender sends a final acknowledgment, and the connection is closed.

---

## UDP

**UDP** stands for **User Datagram Protocol**.

Unlike TCP, UDP is a **connectionless protocol** and does not establish a dedicated connection before transmitting data.

It does not use mechanisms such as the three-way handshake and does not keep track of whether the transmitted data reaches the receiver successfully.

Because of this behavior, UDP is often referred to as the **"Fire and Forget" protocol**.

You can think of UDP as sending data without waiting for confirmation that it has arrived.

UDP is generally **faster than TCP** because it prioritizes **speed over reliability**.

### Common Use Cases of UDP

UDP is commonly used in applications where low latency is more important than guaranteed delivery, such as:

* Live video streaming
* Online gaming
* VoIP calls
* DNS queries
* Real-time communication applications




