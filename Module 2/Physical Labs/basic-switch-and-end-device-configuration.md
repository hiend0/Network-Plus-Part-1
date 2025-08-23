# 2.9.2 Lab - Basic Switch and End Device Configuration

## Topology & Addressing Table

| Device | Interface | IP Address     | Subnet Mask     |
|--------|-----------|----------------|------------------|
| S1     | VLAN 1    | 192.168.1.1    | 255.255.255.0    |
| S2     | VLAN 1    | 192.168.1.2    | 255.255.255.0    |
| PC-A   | NIC       | 192.168.1.10   | 255.255.255.0    |
| PC-B   | NIC       | 192.168.1.11   | 255.255.255.0    |

---

## Objectives

- Set Up the Network Topology  
- Configure PC Hosts  
- Configure and Verify Basic Switch Settings

---

## Background / Scenario

In this lab, you will build a simple network with two hosts and two switches. You will configure basic settings including hostname, local passwords, and login banner. Use `show` commands to display the running configuration, IOS version, and interface status. Use the `copy` command to save device configurations.  
You will apply IP addressing to the PCs and switches to enable communication between the devices. Use the `ping` utility to verify connectivity.

---

## Required Resources

- 2 Switches (Cisco 2960 or comparable)  
- 2 PCs (with terminal emulation software)  
- Console cables  
- Ethernet cables

---

## Instructions

### Step 1: Set Up the Network Topology

- Power on the devices  
- Connect the two switches  
- Connect the PCs to their respective switches  
- Visually inspect network connections  

**Screenshot Placeholder:**  
`!Network Topology`

---

### Step 2: Configure PC Hosts

- Configure static IP address information on the PCs according to the Addressing Table  
- Verify PC settings and connectivity  

**Screenshot Placeholder:**  
`!PC IP Configuration`
![alt text](<Basic Switch Lab.PNG>)
---

### Step 3: Configure and Verify Basic Switch Settings

1. Console into the switch and enter global configuration mode  
2. Set hostname according to the Addressing Table  
3. Disable DNS lookups  
4. Set local passwords:  
   - Privileged EXEC password: `class`  
   - Console access password: `cisco`  
5. Configure and enable the SVI  
6. Set a login MOTD banner  
7. Save the configuration  
8. Display current configuration  
9. Display IOS version and switch info  
10. Display interface status  
11. Configure switch S2  
12. Record interface status:

| Interface | S1 Status | S1 Protocol | S2 Status | S2 Protocol |
|-----------|-----------|-------------|-----------|-------------|
| F0/1      |    up       |      up       |  up         |    up         |
| F0/6      |   up        |       up      |   down        |    down         |
| F0/18     |      down     |    down         |    up       |     up        |
| VLAN 1    |       up    |       up      |    up       |    up         |

---

### Step 4: Verify Connectivity

- From a PC, ping S1 and S2  
  _Were the pings successful?_  
  _Answer:_ 
  The pings were successful

- From a switch, ping PC-A and PC-B  
  _Were the pings successful?_  
  _Answer:_ 
  The pings were successful 

---

## Reflection Questions

1. **Why are some FastEthernet ports on the switches up and others down?**  
   _Answer:_  
   FastEthernet ports are up when a cable is connected. If not connected or administratively disabled, the ports will remain down.  

2. **What could prevent a ping from being sent between the PCs?**  
   _Answer:_  
   There's several factors that could prevent a ping from being sent like faulty cables, bad network ports, wrong IP adress or subnet mask, firewall, switch or router misconfiguration, and more.

   # Lab Summary
   During this lab I learn a lot about connecting physical switches to the computer. I learn how to use PuTTy for the first time. Learning different commands for displaying running configuration, IOS version, and interface status. The biggest struggle I had was researching the commands I needed to complete the lab. 
