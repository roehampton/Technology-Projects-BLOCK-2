# 🏢 Activity 1: Building a Basic LAN

## 🎯 Objective
Set up a simple Local Area Network (LAN) in the Admin Building using *Cisco Packet Tracer*. You will connect multiple PCs to a switch, assign IP addresses, and test connectivity using `ping`.

---

## 🧰 What You’ll Need
- Cisco Packet Tracer
- Basic understanding of IP addressing
- Familiarity with Packet Tracer interface

---

## 🗺️ Scenario
You are the network technician for the Admin Building of a university campus. Your task is to set up a small LAN for five administrative staff members. Each staff member has a PC that needs to be connected to the network.

---

## 🛠️ Step-by-Step Instructions

### Step 1: Create the Network Topology
1. Open Packet Tracer.
2. From the **End Devices** section, drag **5 PCs** onto the workspace.
3. From the **Switches** section, drag **1 switch** (e.g., `2960`) onto the workspace.
4. Use **Copper Straight-Through cables** to connect each PC to the switch:
   - PC0 → Switch (FastEthernet0/1)
   - PC1 → Switch (FastEthernet0/2)
   - PC2 → Switch (FastEthernet0/3)
   - PC3 → Switch (FastEthernet0/4)
   - PC4 → Switch (FastEthernet0/5)

---

### Step 2: Assign IP Addresses
Use the IP range `192.168.1.0/24`. Assign the following IPs manually:

| Device | IP Address     | Subnet Mask     |
|--------|----------------|-----------------|
| PC0    | 192.168.1.10   | 255.255.255.0   |
| PC1    | 192.168.1.11   | 255.255.255.0   |
| PC2    | 192.168.1.12   | 255.255.255.0   |
| PC3    | 192.168.1.13   | 255.255.255.0   |
| PC4    | 192.168.1.14   | 255.255.255.0   |

To assign IPs:
1. Click on a PC.
2. Go to the **Desktop** tab → **IP Configuration**.
3. Enter the IP address and subnet mask.

---

### Step 3: Test Connectivity
1. Open the **Command Prompt** on each PC.
2. Use the `ping` command to test connectivity between PCs:
   - Example: `ping 192.168.1.11` from PC0.
3. Try pinging all other PCs from each device.
4. Finally, try with a non-existing IP, like `ping 192.168.1.15`

✅ **Expected Result**: All pings should be successful, indicating proper LAN connectivity, except for the last one.

---

## 🧠 Reflection Questions
1. What would happen if two PCs had the same IP address?
If two computers have the same IP address it could lead to packets loss and some other consequences.
2. Why do we use a switch instead of connecting PCs directly?
Connecting using switches makes connect a lagre amount of PCs together easier, as it acts as a central hub for all of the computers.
3. What does the subnet mask `255.255.255.0` mean?
The subnet mask '255.255.255.0' tell the comptuer which part of the IP address identifies the network and which part identifies an individual device.

---

## 🏁 Completion Criteria
- All PCs are connected to the switch.
- IPs are correctly assigned.
- All devices can ping each other successfully.
