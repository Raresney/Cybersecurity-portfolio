# LAN Topologies

Over the years, there has been experimentation and implementation of various network designs. In reference to networking, when we refer to the term **"topology"**, we are actually referring to the design or look of the network at hand.

## Ring Topology

A **ring topology** works by sending data across the loop until it reaches the destined device, using other devices along the loop to forward the data. Interestingly, a device will only send received data from another device in this topology if it does not have any to send itself. If the device happens to have data to send, it will send its own data first before sending data from another device.

## Switches

**Switches** are dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet. These various devices plug into a switch's port. Switches are usually found in larger networks such as businesses, schools, or similar-sized networks, where there are many devices to connect to the network.

Switches can connect a large number of devices by having ports of **4, 8, 16, 24, 32, and 64** for devices to plug into.

## Address Resolution Protocol (ARP)

Each device within a network has a ledger to store information on, which is called a **cache**. In the context of ARP, this cache stores the identifiers of other devices on the network.

In order to map two identifiers together (IP address and MAC address), ARP sends two types of messages:

- **ARP Request**
- **ARP Reply**

## DHCP (Dynamic Host Configuration Protocol)

IP addresses can be assigned either manually, by entering them physically into a device, or automatically and most commonly by using a **DHCP server**.

The DHCP process follows four steps:

1. **DHCP Discover** - Device sends out a request to see if any DHCP servers are on the network
2. **DHCP Offer** - The DHCP server replies back with an IP address the device could use
3. **DHCP Request** - The device sends a reply confirming it wants the offered IP address
4. **DHCP ACK** - The DHCP server sends a reply acknowledging this has been completed, and the device can start using the IP address

## OSI Model

The **OSI model** (Open Systems Interconnection Model) is an essential model used in networking. This critical model provides a framework dictating how all networked devices will send, receive, and interpret data.

| Layer | Name |
|-------|------|
| 7 | Application |
| 6 | Presentation |
| 5 | Session |
| 4 | Transport |
| 3 | Network |
| 2 | Data Link |
| 1 | Physical |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
