### **1. General Overview**
- **Core Routers:** The three routers (labeled `f1-Router2`, `f2-Router1`, and `f3-Router0`) form the backbone of the network, connecting the different segments. These routers are connected via `10.10.10.x/30` subnets, typically used for point-to-point connections between routers.
  
- **VLANs (Virtual LANs):** VLANs are used to segment the network into different broadcast domains. Each VLAN has its own subnet.

### **2. Network Segments (by Color and VLANs)**

#### **Blue Segment (Likely 2nd Floor)**
- **Devices:**
  - Several PCs, printers, an access point, and a router (`f2-Router1`) are connected through a `2960-24TT` switch.
  - The VLANs here are:
    - **VLAN 30 (192.168.3.0/24):** Connected to sales devices.
    - **VLAN 40 (192.168.4.0/24):** Connected to HR devices.
    - **VLAN 50 (192.168.5.0/24):** Connected to finance devices.

- **Purpose:** This segment likely serves multiple departments such as Sales, HR, and Finance. Each department has its own VLAN, ensuring traffic isolation for better security and network efficiency.

#### **Green Segment (Likely 3rd Floor - IT Department)**
- **Devices:**
  - PCs, printers, smartphones, tablets, and a `2960-24TT` switch are connected to `f3-Router0`.
  - The VLANs here are:
    - **VLAN 10 (192.168.1.0/24):** IT department devices.
    - **VLAN 20 (192.168.2.0/24):** Admin department devices.

- **Purpose:** This segment is likely for the IT department and administrative purposes, ensuring that these critical departments have their own isolated network resources.

#### **Pink Segment (Likely 1st Floor)**
- **Devices:**
  - PCs, printers, access points, and various mobile devices are connected through a `2960-24TT` switch.
  - The VLANs here are:
    - **VLAN 70 (192.168.7.0/24):** Logistics department devices.
    - **VLAN 80 (192.168.8.0/24):** Devices for the reception and other unspecified departments.

- **Purpose:** This segment likely serves the reception area, logistics, and other departments on the 1st floor. It also features wireless connectivity through access points, serving mobile devices such as laptops, tablets, and smartphones.

### **3. Routing Between VLANs**
- **Inter-VLAN Routing:** The routers (`f1-Router2`, `f2-Router1`, and `f3-Router0`) handle routing between different VLANs, allowing devices in different VLANs to communicate when necessary.

### **4. Device Connections**
- **Access Points:** Wireless devices (laptops, smartphones, tablets) are connected to the network via access points. This allows for mobile devices to connect to the wired network infrastructure.
  
- **PCs and Printers:** Each segment has PCs and printers that are connected via switches. The printers are likely network printers shared by the PCs within the same VLAN.

### **5. Summary**
- **Purpose of the Network:** This network is designed to support a multi-floor or multi-department organization with clearly defined network segments. Each department or floor has its own VLAN to manage traffic efficiently and securely. Routers connect these VLANs and allow for controlled inter-VLAN communication.
