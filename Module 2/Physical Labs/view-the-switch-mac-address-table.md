# 7.3.7 Lab - View the Switch MAC Address Table

## Topology & Addressing Table

| Device | Interface | IP Address     | Subnet Mask     |
|--------|-----------|----------------|------------------|
| S1     | VLAN 1    | 192.168.1.11   | 255.255.255.0    |
| S2     | VLAN 1    | 192.168.1.12   | 255.255.255.0    |
| PC-A   | NIC       | 192.168.1.1    | 255.255.255.0    |
| PC-B   | NIC       | 192.168.1.2    | 255.255.255.0    |

---

## Objectives

- **Part 1:** Build and Configure the Network  
- **Part 2:** Examine the Switch MAC Address Table

---

## Part 1: Build and Configure the Network

### Step 1: Cable the network according to the topology

**Screenshot Placeholder:**  
`!Network Topology`

---

### Step 2: Configure PC hosts

**Screenshot Placeholder:**  
`![PC Configuration](path/to/sStep 3: Initialize and reload switches as necessary

**Screenshot Placeholder:**  
`!Switch Initialization`

---

### Step 4: Configure basic settings for each switch

- **Device name**  
- **IP address**  
- **Console and vty passwords: `cisco`**  
- **Privileged EXEC password: `class`**

---

## Part 2: Examine the Switch MAC Address Table

### Step 1: Record network device MAC addresses

1. **PC-A MAC Address:**  
   _Answer:_  

2. **PC-B MAC Address:**  
   _Answer:_  

3. **S1 Fast Ethernet 0/1 MAC Address:**  
   _Answer:_  

4. **S2 Fast Ethernet 0/1 MAC Address:**  
   _Answer:_  

---

### Step 2: Display the switch MAC address table

1. **Are there any MAC addresses recorded in the MAC address table?**  
   _Answer:_  
   If there's traffic flowing through the switch, the switch should have some MAC addresses listed. It's likely that the switch has learned MAC addresses via the F0/1 port on S1. If the switch has learn any other MAC addresses through actice traffic like pings or other communication, those address will be listed. 

2. **What MAC addresses are recorded in the table? To which switch ports are they mapped and to which devices do they belong?**  
   _Answer:_  
   The S1 F0/1 MAC address and PC-A MAC are mapped to S2 F0/1.

3. **If you had not previously recorded MAC addresses of network devices in Step 1, how could you tell which devices the MAC addresses belong to using only the output from `show mac address-table`? Does it work in all scenarios?**  
   _Answer:_ 
   While the show MAC address table command provides usefull information about the MAC address learned on each port, it does not always work in all scenarios. Especially when multiple MAC addresses share a port or if the switch hasn't learned or refreshed the MAC address table.   

---

### Step 3: Clear the S2 MAC address table and display the MAC address table again

1. **Does the MAC address table have any addresses in it for VLAN 1? Are there other MAC addresses listed?**  
   _Answer:_  
   No. If there were other MAC addresses it would be displayed separately under their own VLAN IDs. 

2. **Wait 10 seconds and recheck. Are there new addresses in the MAC address table?**  
   _Answer:_  

---

### Step 4: From PC-B, ping the devices on the network and observe the switch MAC address table
1. **How many device IP-to-MAC address pairs have been learned by ARP (excluding multicast/broadcast)?**  
   _Answer:_  

2. **Did all devices have successful replies to pings? If not, check cabling and IP configurations.**  
   _Answer:_  
   Yes, cables and IP configurations were done correctly.

3. **Has the switch added additional MAC addresses to the MAC address table? If so, which addresses and devices?**  
   _Answer:_  

4. **Does the PC-B ARP cache have additional entries for all network devices that were sent pings?**  
   _Answer:_  

---

## Reflection Question

**What might be some of the challenges on larger networks when switches and PCs dynamically build ARP caches and MAC address tables?**  
_Answer:_  
In a larger network means large numbers of devices. A large number of devices means more ARP requests, leading to an ARP flood. Which will increase the load of the network device and can reduce performance. Mac address table will expand from a larger network, which mean the switch must store more MAC addresses in their table. 

# Lab Summary

