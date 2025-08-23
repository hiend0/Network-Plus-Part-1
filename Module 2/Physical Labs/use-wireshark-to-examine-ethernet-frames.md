# 7.1.6 Lab - Use Wireshark to Examine Ethernet Frames

## Objectives

- **Part 1:** Examine the Header Fields in an Ethernet II Frame  
- **Part 2:** Use Wireshark to Capture and Analyze Ethernet Frames

---

## Part 1: Examine the Header Fields in an Ethernet II Frame

### Step 1: Review the Ethernet II header field descriptions and lengths

| Field               | Length         |
|--------------------|----------------|
| Preamble            | 8 Bytes        |
| Destination Address | 6 Bytes        |
| Source Address      | 6 Bytes        |
| Frame Type          | 2 Bytes        |
| Data                | 46–1500 Bytes  |
| FCS                 | 4 Bytes        |

---

### Step 2: Examine the network configuration of the PC

**Screenshot Placeholder:**  
`!ipconfig output`
![alt text](<7.1.6 Lab Module 2 2.png>)

---

### Step 3: Examine Ethernet frames in a Wireshark capture

**Screenshot Placeholder:**  
`![ARP request frame](path/to/screenshot`

![alt text](<7.1.6 Lab Module 2.png>)
---

### Step 4: Examine the Ethernet II header contents of an ARP request

1. **What is significant about the contents of the destination address field?**  
   _Answer:_  
   The destination address field is significant because it tells the network where the packet is suppose to go. The host with the IP address 192.168.1.1 will send a reply to the source.

2. **Why does the PC send out a broadcast ARP prior to sending the first ping request?**  
   _Answer:_  
   When a PC wants to send its first ping to another device on the same LAN, it must know the MAC address of the destination. The ARP broadcast is used to request the MAC address of the host.

3. **What is the MAC address of the source in the first frame?**  
   _Answer:_  
   MAC address is bc:c7:46:a2:f4:ca

4. **What is the Vendor ID (OUI) of the Source NIC in the ARP reply?**  
   _Answer:_  
   HonHaiPrecis

5. **What portion of the MAC address is the OUI?**  
   _Answer:_  
   First 3 octets

6. **What is the NIC serial number of the source?**  
   _Answer:_  
   a2:f4:ca

---

##