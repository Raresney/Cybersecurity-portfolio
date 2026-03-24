# Packets and Frames

## Overview

**Packets** and **frames** are small pieces of data that, when forming together, make a larger piece of information or message. However, they are two different things in the OSI model.

- A **packet** is a piece of data from **Layer 3 (Network Layer)** of the OSI model, containing information such as an IP header and payload.
- A **frame** is used at **Layer 2 (Data Link)** of the OSI model, which encapsulates the packet and adds additional information such as MAC addresses.

You can think of this process as similar to mailing a letter through the post. The envelope is a frame, which is used to move the contents (the packet) to another place. Once the recipient opens the envelope (frame), they will know how to forward the letter (packet) itself.

## Encapsulation

This process is called **encapsulation**. At this stage, it's safe to assume that when we are talking about anything IP addresses, we are talking about packets. When the encapsulating information is stripped away, we're talking about the frame itself.

## Why Packets?

Packets are an efficient way of communicating data across networked devices. Because this data is exchanged in small pieces, there is less chance of **bottlenecking** occurring across a network than large messages being sent at once.

For example, when loading an image from a website, this image is not sent to your computer as a whole, but rather small pieces where it is reconstructed on your computer.

## TCP (Transmission Control Protocol)

**TCP** is another one of the rules used in networking. Packets have different structures that are dependent upon the type of packet that is being sent.

## TCP/IP Model

This protocol is very similar to the OSI model. The TCP/IP protocol consists of **four layers** and is arguably just a summarised version of the OSI model:

| Layer | Name |
|-------|------|
| 4 | Application |
| 3 | Transport |
| 2 | Internet |
| 1 | Network Interface |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
