# Packet Tracer – Implement VLANs and Trunking

## Objectives
- Part 1: Configure VLANs  
- Part 2: Assign Ports to VLANs  
- Part 3: Configure Static Trunking  
- Part 4: Configure Dynamic Trunking  

---

## Addressing Table
| Device | Interface | IP Address     | Subnet Mask     | Switchport | VLAN  |
|--------|-----------|----------------|-----------------|------------|-------|
| PC1    | NIC       | 192.168.10.10  | 255.255.255.0   | SWB F0/1   | 10    |
| PC2    | NIC       | 192.168.20.20  | 255.255.255.0   | SWB F0/2   | 20    |
| PC3    | NIC       | 192.168.30.30  | 255.255.255.0   | SWB F0/3   | 30    |
| PC4    | NIC       | 192.168.10.11  | 255.255.255.0   | SWC F0/1   | 10    |
| PC5    | NIC       | 192.168.20.21  | 255.255.255.0   | SWC F0/2   | 20    |
| PC6    | NIC       | 192.168.30.31  | 255.255.255.0   | SWC F0/3   | 30    |
| PC7    | NIC       | 192.168.10.12  | 255.255.255.0   | SWC F0/4   | 10    |
| SWA    | SVI       | 192.168.99.252 | 255.255.255.0   | N/A        | 99    |
| SWB    | SVI       | 192.168.99.253 | 255.255.255.0   | N/A        | 99    |
| SWC    | SVI       | 192.168.99.254 | 255.255.255.0   | N/A        | 99    |

---

## VLAN Table
| VLAN Number | VLAN Name   |
|-------------|-------------|
| 10          | Admin       |
| 20          | Accounts    |
| 30          | HR          |
| 40          | Voice       |
| 99          | Management  |
| 100         | Native      |

---

## Instructions

### Part 1: Configure VLANs
- Configure VLANs on all three switches based on the VLAN Table.  
- VLAN names must match exactly.  

### Part 2: Assign Ports to VLANs
1. Assign access ports on SWB and SWC according to the Addressing Table.  
2. Configure the voice VLAN port on SWC.  
3. Create and address the virtual management interfaces (SVIs) on all three switches.  
   - Use the IPs from the Addressing Table.  
   - The switches should **not** be able to ping each other.  

### Part 3: Configure Static Trunking
- Configure the link between SWA and SWB as a static trunk.  
- Disable DTP on both ends of the trunk link.  
- Configure the trunk with the native VLAN and resolve any conflicts.  

### Part 4: Configure Dynamic Trunking
- On SWA, configure G0/2 so it negotiates trunking with SWC.  
- Configure the trunk with the native VLAN and resolve any conflicts.  

---

## How to Use
- Open the `.pkt` file in Cisco Packet Tracer.  
- Follow the steps above to configure VLANs and trunking.  
