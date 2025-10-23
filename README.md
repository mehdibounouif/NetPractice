# 🌐 NetPractice — Networking Fundamentals (42 Project)

Welcome to **NetPractice**, an interactive project from **42 School** that helps you learn how computer networks work — one IP, one subnet, and one packet at a time.

This guide walks you through the key networking concepts that you’ll need to understand and apply in this project.

---

## 🧩 What Is an IP?

An **IP (Internet Protocol) address** is a unique numerical label assigned to each device connected to a network.  
It identifies:
1. **The host** (specific device)  
2. **The network** it belongs to  

Think of it like a home address — it tells data where to go on the internet.

---

## 🗂️ Types of IP Addresses

| Type | Description |
|------|--------------|
| **Private IP** | Used within local networks (e.g., 192.168.x.x). Not visible on the internet. |
| **Public IP** | Unique across the internet. Assigned by your ISP. |
| **Static IP** | Manually configured and doesn’t change. |
| **Dynamic IP** | Assigned automatically by DHCP and can change over time. |
| **Loopback IP** | Used for internal testing (127.0.0.1). |

---

## 🎯 Purpose of IP Addresses

IP addresses allow devices to **find** and **communicate** with each other over networks.  
Every email sent, every website visited, and every online message relies on IP addressing to reach the correct destination.

---

## 🌍 IPv4 vs IPv6

| Feature | **IPv4** | **IPv6** |
|----------|-----------|-----------|
| **Format** | 32-bit (e.g., `192.168.1.1`) | 128-bit (e.g., `2001:0db8:85a3::8a2e:0370:7334`) |
| **Total Addresses** | ~4.3 billion | ~340 undecillion |
| **Notation** | Dotted decimal | Hexadecimal with colons |
| **Purpose** | Traditional system, still widely used | Created to solve IPv4 exhaustion and improve efficiency |

---

## 🖧 What Is TCP/IP?

**TCP/IP (Transmission Control Protocol / Internet Protocol)** is the fundamental suite of communication protocols used for the Internet and most networks.

- **IP** defines *where* data goes (addressing and routing).  
- **TCP** defines *how* data is transmitted reliably between systems.

Together, they make sure your data reaches the right place **accurately and in order**.

---

## ⚙️ Difference Between TCP and IP

| Concept | **TCP** | **IP** |
|----------|----------|--------|
| **Function** | Ensures reliable communication and correct order of data packets. | Handles addressing and routing of packets across networks. |
| **Level** | Transport layer | Network layer |
| **Reliability** | Reliable (checks for errors and retransmits lost packets) | Unreliable (best effort delivery) |

---

## 🔄 How TCP/IP Works

1. **Application Layer** – Your app (like a browser) creates data to send.  
2. **Transport Layer (TCP)** – Splits data into segments, adds port numbers, and ensures reliability.  
3. **Internet Layer (IP)** – Adds IP addresses to define source and destination.  
4. **Network Access Layer** – Converts data into bits and sends it physically through cables or Wi-Fi.  
5. **Destination Device** – Reassembles and reads the data in the correct order.

---

## 🔌 What Is a Switch?

A **switch** connects multiple devices on the same local network (LAN) and forwards data only to the device that needs it.  
It operates on **Layer 2 (Data Link Layer)** using **MAC addresses**.

Think of it like a traffic controller inside your local network.

---

## 🚦 What Is a Router?

A **router** connects multiple networks together (like your home network and the internet).  
It operates on **Layer 3 (Network Layer)** and uses **IP addresses** to determine the best path for data packets.

---

## 🛰️ How a Router Works

1. Receives data packets from one network.  
2. Reads their **destination IP address**.  
3. Uses its **routing table** to decide the best path.  
4. Forwards the packets to the next hop (another router or the destination device).

Routers make the internet possible by guiding billions of packets every second.

---

## 📡 Modem vs Router

| Feature | **Modem** | **Router** |
|----------|------------|-------------|
| **Purpose** | Connects your network to your ISP (Internet Service Provider). | Distributes the internet connection to multiple devices. |
| **Function** | Converts signals between your ISP and your network. | Directs traffic between your devices and external networks. |
| **Typical Connection** | One-to-one (ISP ↔ Modem) | One-to-many (Router ↔ Devices) |

---

## 🌀 What Is a Loopback Address?

The **loopback address** (typically `127.0.0.1` for IPv4 or `::1` for IPv6) is used to test network functionality **within your own computer**.  
It never leaves the machine — perfect for testing servers locally.

---

## 🧮 What Is a Subnet?

A **subnet (subnetwork)** divides a large network into smaller, more manageable parts.  
This improves performance, security, and efficiency by reducing congestion and limiting broadcast traffic.

Example:  
`192.168.1.0/24` → 256 possible addresses within that subnet.

---

## 🧠 How to Calculate a Subnet Mask (Step by Step)

Let’s take an example: `192.168.1.10/26`

1. **Write the CIDR notation**: `/26` means the first 26 bits are network bits.  
2. **Convert to binary mask**:
```
11111111.11111111.11111111.11000000
```
3. **Convert to decimal**:
```
255.255.255.192
```

4. **Find the block size**:  
`256 - 192 = 64`
5. **Find subnet ranges**:
- 192.168.1.0 → Network address  
- 192.168.1.1 – 192.168.1.62 → Usable hosts  
- 192.168.1.63 → Broadcast address

✅ Your subnet mask: **255.255.255.192**  
✅ 62 usable hosts per subnet

---

## 🚀 Summary

NetPractice helps you **visualize and master** these networking fundamentals by simulating real network configurations.  
By the end, you’ll understand how **data travels**, **networks interconnect**, and **IPs communicate** — all crucial skills for any developer or system engineer.

---

## 🧭 Author

**Project:** NetPractice  
**School:** 42  
**Written by:** *[Your Name]*  
**Date:** *[Month, Year]*  

---

> _“The network is the computer.” – John Gage_

