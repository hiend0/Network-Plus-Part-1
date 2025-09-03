# 🧪 Lab: Investigating the ARP Table and Protocol 

## 🧭 Objective

This lab will guide you through:
- Viewing and understanding the ARP table on a Windows machine.
- Selecting a target device on your home network.
- Clearing the ARP cache.
- Capturing ARP traffic using Wireshark.

---

## 🛠️ Prerequisites

- A Windows PC with administrative privileges.
- Wireshark installed.
- At least one other device connected to the same local network.
- Basic understanding of networking concepts (Layer 2, MAC addresses, IP addresses).

---

## 🔍 Step 1: View the ARP Table
1. Open **Command Prompt** as Administrator.
2. Run the following command:

   ```cmd
   arp -a
   ```
3. Observe the output. You should see a list of IP addresses and their corresponding MAC addresses.

![Insert Screenshot Here]()
![alt text](<ARP table.PNG>)
## 🎯 Step 2: Identify a Target Device
1. Choose another device on your network (e.g., phone, tablet, another PC).
2. Find its IP address:
    - On Windows: open CMD and run `ipconfig` 
    - On MAC or Linux: open terminal and run `ip a`
    - On iOS or Android: check Wi-Fi settings 
3. Ping the device from your Windows machine:
    ```CMD
    ping <target IP>
    ```
4. Run the `arp -a` command again to confirm the target device appears in the ARP table

![Insert screenshot here]()
![alt text](<ARp Table 1.PNG>)
![alt text](<ARp Table 2.PNG>)

## 🧪 Step 3: Capture ARP Traffic with Wireshark

1. Open Wireshark and start capturing on your active network interface.
2. In the Display Filter, enter: `arp` 
3. Clear the entire ARP cache 
    ```CMD
    netsh interface ip delete arpcache 
    ```
4. Ping target device again 
    ```CMD
    ping <target IP>
    ```
5. Observe ARP request and reply packets in Wireshark 

![Insert screenshot here]()
![alt text](<ARp Table 3.PNG>)
![alt text](<ARp Table 4.PNG>)

***

## 🧠 Reflection Questions
1. What does the ARP table tell you about your local network?

ARP tables shows the IP addresses and MAC addresses on your network that your device has recently communicated with.

2. Why might an ARP entry be missing?

There are several ways an ARP entry can be missing like target host is down, configuration error like submask and DHCP issues, network path issues and more.

3. What happens when you clear the ARP cache?

When clearing the ARP cache this will remove existing IP-to-MAC address mapping from the device memory. 

4. How does Wireshark help visualize Layer 2 communication?

Wireshark visualize Layer 2 communication by breaking down network frames it captures. It shows the details like the Ethernet header in the packet detail pane. 