# ICMP

> **ICMP** stands for **Internet Control Message Protocol**.

ICMP is a protocol that operates at the **Network Layer (Layer 3)** of the OSI model.

### Key Points

* Used for **error reporting** and **network diagnostics**.
* Helps devices communicate information about network conditions.
* ICMP is **not designed to carry application data** like TCP or UDP.
* Commonly used by network utilities such as `ping` and `traceroute`.

---

# PING

> **Ping** is a utility used to check whether a host is reachable over a network.

### How Ping Works

Ping uses ICMP messages:

1. The source sends an **ICMP Echo Request**.
2. The destination responds with an **ICMP Echo Reply**.
3. The source measures the **Round-Trip Time (RTT)**.

```text
You → ICMP Echo Request → Server
You ← ICMP Echo Reply   ← Server
```

### Use Cases

* **Host discovery**
* Checking **network connectivity**
* Basic **network troubleshooting**
* Measuring **Round-Trip Time (RTT)**
* Identifying whether **ICMP traffic is being filtered**

> **Note:** A failed ping does not always mean that a host is down. The host may simply be configured to block or ignore ICMP Echo Requests.

---

# TRACEROUTE

> **Traceroute** is a network diagnostic utility used to discover the **network path (hops)** between a source and a destination.

It works by manipulating the **TTL (Time To Live)** value in IP packets.

### Example

```text
You → Router 1 → Router 2 → Router 3 → Server
        ↓          ↓          ↓
       TTL 1      TTL 2      TTL 3
```

### How It Works

The sender initially sends a packet with a low TTL value.

```text
TTL = 1
```

When Router 1 processes the packet, the TTL is decremented:

```text
TTL = 0
```

The router discards the packet and normally sends an:

> **ICMP Time Exceeded**

message back to the sender.

Traceroute then increases the TTL:

```text
TTL = 1 → Discover Router 1
TTL = 2 → Discover Router 2
TTL = 3 → Discover Router 3
...
```

This allows traceroute to build a view of the path toward the destination.

---

## Cybersecurity Use Cases

Traceroute can be useful for:

* **Mapping network paths**
* Understanding **network topology**
* Troubleshooting **routing problems**
* Identifying **intermediate infrastructure**
* Understanding how traffic travels between networks

---

## Quick Comparison

| Tool         | Protocol / Mechanism           | Main Purpose                    |
| ------------ | ------------------------------ | ------------------------------- |
| `ping`       | ICMP Echo Request/Reply        | Check host reachability and RTT |
| `traceroute` | TTL + ICMP responses           | Discover network path/hops      |
| ICMP         | Network-layer control protocol | Error reporting and diagnostics |

---

### Key Takeaway

**ICMP** provides network-layer control and diagnostic messages.

**Ping** uses ICMP Echo Request/Reply to test reachability and measure RTT.

**Traceroute** manipulates TTL values and uses responses such as **ICMP Time Exceeded** to discover the path between two hosts.
