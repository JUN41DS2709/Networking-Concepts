# DNS

**DNS stands for Domain Name System.**

- It's like the phone book of the Internet.
- What it does is resolve a domain name into an IP address.

**Example:**

```text
https://example.com  →  93.184.216.34
```

---

# Working of DNS

You request **example.com**

↓

DNS first checks its **DNS cache** (browser cache, operating system cache, etc.) to see if there is a previous record for the domain. If there is, it quickly returns the IP address.

If there isn't, it sends the request to the **DNS Recursor (Recursive Resolver).**

↓

The **DNS Recursive Resolver** is like an assistant that searches for the domain's address for you.

It says:

> "I don't have the address, but I'll find it for you!"

↓

The DNS Recursor goes to the **Root Server**.

The Root Server knows where all the **Top-Level Domain (TLD)** servers are located.

It says:

> "I don't have the IP address, but ask the **.com** TLD server."

↓

The Root Server provides the address of the **.com TLD Server**.

The TLD Server then says:

> "I don't have the IP address either, but I know which **Authoritative DNS Server** manages this domain. Go there."

↓

The DNS Recursor then goes to the **Authoritative DNS Server**, which stores the DNS records for the requested domain.

It replies:

> "Here is the IP address: **93.184.216.34**"

↓

The DNS Recursor returns the IP address to your computer, stores it in its cache for future requests, and finally **example.com** loads in your browser.

---

# DNS Records

When we search for something on the Internet, the response we get is possible because of **DNS records**.

For example:

When we search **example.com**, DNS looks up the required record (usually an **A** or **AAAA** record) and returns the IP address so the browser knows where to connect.

DNS records store different types of information, and each record has its own purpose.

There are **5 main types of DNS records** that help things work smoothly on the Internet.

## A Record

- An **A Record** maps a domain name to an **IPv4 address**.

Example:

```text
example.com    IN    A    192.168.1.1
```

It resolves the domain name to its IPv4 address.

---

## AAAA Record

- An **AAAA Record** is similar to an A Record, but it maps a domain name to an **IPv6 address**.

Example:

```text
example.com    IN    AAAA    2606:4700:4700::1111
```

It resolves the domain name to its IPv6 address.

---

## MX Record

- An **MX (Mail Exchange) Record** tells the Internet where emails for a domain should be delivered.

Think of it like a mailbox outside a house.

- The **house** is the organization.
- The **mailbox** is the mail server.

Anyone sending an email to the organization knows exactly where to deliver it.

Example:

```text
example.com    IN    MX    10    mail.example.com
```

---

## CNAME Record

- A **CNAME (Canonical Name) Record** creates an alias (nickname) for another domain name.

Think of it as giving one domain another name that points to the original domain.

Example:

```text
www.example.com    IN    CNAME    example.com
```

or

```text
blog.example.com    IN    CNAME    username.github.io
```

---

## TXT Record

- A **TXT Record** stores arbitrary text for verification and security purposes.

It is commonly used for:

- Domain ownership verification
- SPF
- DKIM
- DMARC

Think of it like this:

You own a house, and a real estate company comes to verify that it really belongs to you.

They tell you:

> "Place this secret message outside your house. When we visit, we'll check if it's there to verify your ownership."

DNS works in a similar way.

Example:

```text
example.com    IN    TXT    "google-site-verification=xxxx"
```

---

# Summary

DNS is responsible for translating human-readable domain names into IP addresses so computers can communicate with each other.

The DNS resolution process follows this order:

```text
Client
   ↓
DNS Cache
   ↓
Recursive Resolver
   ↓
Root Server
   ↓
TLD Server
   ↓
Authoritative DNS Server
   ↓
IP Address Returned
   ↓
Website Loads
```
