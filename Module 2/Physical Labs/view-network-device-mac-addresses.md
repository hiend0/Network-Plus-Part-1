# 7.2.7 Lab - View Network Device MAC Addresses

## Topology & Addressing Table

| Device | Interface | IP Address     | Subnet Mask     | Default Gateway |
|--------|-----------|----------------|------------------|------------------|
| S1     | VLAN 1    | 192.168.1.2    | 255.255.255.0    | N/A              |
| PC-A   | NIC       | 192.168.1.3    | 255.255.255.0    | 192.168.1.1      |

---

## Objectives

- **Part 1:** Configure Devices and Verify Connectivity  
- **Part 2:** Display, Describe, and Analyze Ethernet MAC Addresses

---

## Part 1: Configure Devices and Verify Connectivity

### Step 1: Cable the network as shown in the topology

**Screenshot Placeholder:**  
`!Network Topology`

---

### Step 2: Configure the IPv4 address for the PC

- **Were the pings successful? Explain.**  
  _Answer:_  
  The ping was unsuccessful. The switch hasn't been configured yet.

---

### Step 3: Configure basic settings for the switch

**Screenshot Placeholder:**  
`![Switch Configuration](path/to/screenshoterify network connectivity

- **Were the pings successful?**  
  _Answer:_  
  Yes, the ping was successful

---

## Part 2: Display, Describe, and Analyze Ethernet MAC Addresses

### Step 5: Analyze the MAC address for the PC-A NIC

1. **What is the OUI portion of the MAC address for this device?**  
   _Answer:_  
   5C-26-0A

2. **What is the serial number portion of the MAC address for this device?**  
   _Answer:_  
   24-2A-60

3. **Using the example above, find the name of the vendor that manufactured this NIC.**  
   _Answer:_  
   Dell Inc

4. **Identify the OUI portion of the MAC address for the NIC of PC-A.**  
   _Answer:_  

5. **Identify the serial number portion of the MAC address for the NIC of PC-A.**  
   _Answer:_  

6. **Identify the name of the vendor that manufactured the NIC of PC-A.**  
   _Answer:_  

---

### Step 6: Analyze the MAC address for the S1 VLAN 1 interface

1. **What is the MAC address for VLAN 1 on S1?**  
   _Answer:_  

2. **What is the MAC serial number for VLAN 1?**  
   _Answer:_  

3. **What does BIA stand for?**  
   _Answer:_  
   Burned in address

4. **Why does the output show the same MAC address twice?**  
   _Answer:_  
   Since the MAC address can be changed, the BIA will still be there in parenthesis.
---

### Step 7: View the MAC addresses on the switch

1. **What Layer 2 addresses are displayed on S1?**  
   _Answer:_  
   001b.0c6d.8f40
   5c26.0a24.2a60

2. **What Layer 3 addresses are displayed on S1?**  
   _Answer:_  
   192.168.1.2
   192.168.1.3

3. **Did the switch display the MAC address of PC-A? If yes, what port was it on?**  
   _Answer:_  

---

## Reflection Questions

1. **Can you have broadcasts at the Layer 2 level? If so, what would the MAC address be?**  
   _Answer:_  
   Yes, these broadcast operate at the layer 2 level. ARP will use to find MAC address and DHCP clients broadcast to discover DHCP servers. MAC address is FF:FF:FF:FF:FF:FF.

2. **Why would you need to know the MAC address of a device?**  
   _Answer:_

   Knowing the MAC address of a device can be helpful in serveral reasons. One reason would be great for tracking devices. Network admins may need the MAC address to identify the devices by the manufacturer. MAC address helps with network management, troubleshooting, and security. 

   # Reflective Questions
   In this lab I learn how to anaylze ethernet MAC address. I learned that MAC address OUI shows the manufacturer and I can use an OUI lookup tool to find the vendor. This lab highlighted the importance of MAC addresses in networking. I gained insight into how switches forward data frames and how network admins can use this information for tasks like access control and monitoring network traffic. 

