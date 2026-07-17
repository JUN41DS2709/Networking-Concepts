**# TCP and UDP**



**## TCP**



**TCP stands for \*\*Transmission Control Protocol\*\*.**



**It is a \*\*connection-oriented protocol\*\* which is used for reliable and error-free transmitting of data between the sender and the receiver.**



**It uses a \*\*three-way handshake method\*\* to securely establish a connection and transmit data between devices in the correct order and error-free manner.**



**### TCP uses a three-way handshake method**



**Where:**



**\* \*\*SYN:\*\* A request is sent first to initiate a connection.**

**\* \*\*SYN-ACK:\*\* The server or receiver acknowledges it and sends the acknowledgement back.**

**\* \*\*ACK:\*\* The sender also sends the acknowledgement and the connection is established.**



**After these steps, the data can now be exchanged.**



**### At the time of closing**



**\* \*\*FIN:\*\* TCP sends the FIN to close the connection.**

**\* \*\*FIN-ACK:\*\* The server acknowledges and accepts the request to close the connection.**

**\* \*\*ACK:\*\* The sender sends the ACK and the connection is finally closed.**



**---**



**## UDP**



**UDP stands for \*\*User Datagram Protocol\*\*.**



**Unlike TCP, it is not a connection-oriented protocol but a \*\*connectionless protocol\*\*.**



**It doesn't use any methods like the three-way handshake or establish a dedicated connection.**



**Rather, it just transmits the data and doesn't keep any track of it.**



**It is also known as the \*\*fire and forget protocol\*\*.**



**It's like throwing data in the air expecting it to reach the receiver but not making sure of it.**



**It is faster than TCP because in this protocol \*\*speed matters over quality\*\*.**



**It is mainly used in \*\*live video streaming, gaming, VoIP calls, DNS queries\*\*, etc.**



