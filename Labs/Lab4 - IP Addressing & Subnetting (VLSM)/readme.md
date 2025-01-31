## Lab 4 - IP Addressing and Subnetting (VLSM)

### Overview
Lab 4 covers the implementation of IP addressing and subnetting using Variable Length Subnet Masking (VLSM). The experiments were performed in Cisco Packet Tracer, and the configurations are available in the repository. 🖥️

### Experiments Conducted
1. **IP Address Configuration in a Router**  
   - Assign IP addresses to router interfaces and PCs.
   - Ensure proper communication between networked devices.
   - Implement basic subnetting principles.
   - Use the following commands to configure a router:
     ```
     Router> enable
     Router# configure terminal
     Router(config)# interface GigabitEthernet0/0
     Router(config-if)# ip address 192.168.10.1 255.255.255.0
     Router(config-if)# no shutdown
     Router(config-if)# exit
     Router(config)# exit
     Router# write memory
     ```

2. **Subnetting in WAN Configuration (DTE and DCE)**  
   - Apply VLSM for efficient IP address allocation in a WAN setup.
   - Configure multiple subnets for routers and PCs.
   - Use Serial DCE for inter-router communication.
   - Example command for serial interface:
     ```
     Router(config)# interface Serial0/0/0
     Router(config-if)# ip address 192.168.10.65 255.255.255.224
     Router(config-if)# clock rate 64000
     Router(config-if)# no shutdown
     ```

### Routing Table of the Configured Topology 📜
```
Router# show ip route
Codes: L - local, C - connected, S - static, R - RIP, M - mobile, B - BGP
...
C 192.168.10.0/27 is directly connected, GigabitEthernet0/0
C 192.168.10.32/27 is directly connected, GigabitEthernet0/1
C 192.168.10.64/27 is directly connected, Serial0/0/0
C 192.168.10.96/27 is directly connected, Serial0/0/1
...
```

### Files in This Repository 📂
- **VLSM.pkt** – Packet Tracer file containing the VLSM-based network configuration.
- **VLSM_default.pkt** – A default setup for comparison and learning purposes.
- **README.md** – This documentation.

### Key Learnings ✨
- Importance of subnetting in optimizing IP address usage.
- Configuring routers and PCs with appropriate IP addresses and gateways.
- Using the `show ip route` command to inspect routing tables.
- Understanding WAN connections and serial communication in networking.

Made with ❤️ by Nishant Sheoran

