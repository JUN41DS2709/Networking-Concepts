# IP Address

An **IP Address (Internet Protocol Address)** is a **32-bit logical address** assigned to devices connected to a network so that they can send and receive data over the network.

An IP address uniquely identifies a device connected to a network.

An IPv4 address consists of **4 sets of numbers called octets**.

For example:

```text
192.168.1.100
```

These four sets of numbers separated by dots (`.`) are called **octets**.

Each octet consists of **8 bits**.

```text
8 bits × 4 octets = 32 bits
```

Therefore, an IPv4 address is a **32-bit address**.

---

## Network Portion and Host Portion

An IP address is divided into two parts:

* **Network Portion**
* **Host Portion**

### Network Portion

The part of the IP address that identifies the network uniquely.

### Host Portion

The part of the IP address that identifies the device connected to that network.

---

## House Analogy

Suppose you live in an area identified as:

```text
192.168.1
```

There are multiple houses in this area:

```text
House 1 : 101
House 2 : 102
House 3 : 103
House 4 : 104 (Your House)
```

If someone outside the area wants to send data to you, they first need to know your area:

```text
192.168.1
```

Then they need to know your specific house number:

```text
104
```

Together, your complete address becomes:

```text
192.168.1.104
```

Similarly, on a network:

* `192.168.1` represents the **network portion**.
* `104` represents the **host portion**.

Using IP addresses, devices can communicate, exchange data, browse websites, stream videos, and access online services.

All of this communication is possible because of IP addressing.

---

# Subnet Mask

A **Subnet Mask** is a **32-bit number** used to divide an IP address into two parts:

* Network Portion
* Host Portion

### Network Portion

The portion of the IP address assigned to uniquely identify the network.

### Host Portion

The portion of the IP address assigned to uniquely identify devices connected to that network.

---

# CIDR

**CIDR** stands for **Classless Inter-Domain Routing**.

CIDR notation tells us how much of an IP address belongs to the **network portion** and how much belongs to the **host portion**.

Examples:

```text
/8
/16
/24
```

### Example: `/8`

```text
192.168.1.1/8
```

This tells us that:

* The first octet (8 bits) belongs to the network.
* The remaining three octets belong to the host.

---

### Example: `/16`

```text
192.168.1.1/16
```

This tells us that:

* The first two octets (`8 + 8 = 16 bits`) belong to the network.
* The remaining two octets belong to the host.

---

### Example: `/24`

```text
192.168.1.1/24
```

This tells us that:

* The first three octets (`8 + 8 + 8 = 24 bits`) belong to the network.
* The remaining octet belongs to the host.

---

# IP Address Classes

| First Octet Range | Class |
| ----------------- | ----- |
| 1 – 126           | A     |
| 128 – 191         | B     |
| 192 – 223         | C     |
| 224 – 239         | D     |
| 240 – 255         | E     |

---

## Class A

Class A addresses were designed for **very large networks** covering large geographical areas.

Default subnet:

```text
/8
```

Example:

```text
192.168.1.1/8
```

This means:

* The first octet belongs to the network.
* The remaining three octets belong to the host.

---

## Class B

Class B addresses were designed for **medium-sized networks**.

Default subnet:

```text
/16
```

Example:

```text
192.168.1.1/16
```

This means:

* The first two octets belong to the network.
* The remaining two octets belong to the host.

---

## Class C

Class C addresses were designed for **small-sized networks**.

Default subnet:

```text
/24
```

Example:

```text
192.168.1.1/24
```

This means:

* The first three octets belong to the network.
* The final octet belongs to the host.

---

# Types of IP Address

## Public IP Address

A **Public IP Address** is an IP address that is visible on the Internet.

When you send a request to a website or server, the server does not see your private IP address. Instead, it sees your **public IP address**, which is provided by your **Internet Service Provider (ISP)**.

No matter which website you visit or service you use, your traffic appears to originate from your public IP address.

Example:

```text
129.38.29.00   -> Public IP Address
      |
      |
192.168.1.101  -> Private IP Address
```

---

## Private IP Address

A **Private IP Address** is an IP address used inside local networks such as homes, offices, and organizations.

These addresses are not directly accessible from the Internet.

Devices inside your home network communicate using private IP addresses, while your router uses your public IP address to communicate with the Internet.

Example:

```text
129.38.29.00   -> Public IP Address
      |
      |
192.168.1.101  -> Private IP Address
```

Common private IP ranges are:

```text
10.0.0.0/8
172.16.0.0 - 172.31.255.255
192.168.0.0/16
```

---

## Loopback Address

A **Loopback Address** is an address that sends network traffic back to your own computer.

It is commonly referred to as:

```text
localhost
```

The most commonly used loopback address is:

```text
127.0.0.1
```

Developers, software engineers, game developers, and system administrators use loopback addresses to test applications and services locally without requiring a network connection.

Example uses include:

* Testing web servers.
* Testing APIs.
* Running local databases.
* Software development and debugging.

---

## Summary

* IPv4 addresses are 32 bits long.
* They consist of four 8-bit octets.
* IP addresses are divided into network and host portions.
* Subnet masks determine where this division occurs.
* CIDR notation specifies the number of network bits.
* Public IP addresses are visible on the Internet.
* Private IP addresses are used within local networks.
* Loopback addresses allow a computer to communicate with itself.
