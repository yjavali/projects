# **Design and Implementation of a Secure Corporate Network**

## **Introduction**

This project focuses on designing and implementing a secure corporate network for a medium-sized Manchester-based organisation. The network architecture ensures robust security, scalability, and optimised performance while facilitating secure remote access. Key features include a layered defence approach, VLAN segmentation, and VPN configurations tailored for corporate environments.

The complete project is available at the following secure link: [Access Complete Project](https://drive.proton.me/urls/SN8E45W614#JHapLvBEvOea). The document is password-protected. To request access, please email the author, **Yashas Javali**, stating your purpose. A secure password will be shared upon approval.

---

## **Network Security Architecture**

### **1. Hierarchical Design Principles**
The network follows the **Cisco Hierarchical Design Model**:
- **Core Layer:** Ensures high-speed connectivity and redundancy between the ISP and distribution layers.
- **Distribution Layer:** Manages inter-VLAN routing and serves as the control boundary for security policies.
- **Access Layer:** Provides direct connectivity to end devices, segmented by VLANs for each department.

### **2. VLAN Segmentation**
| **Department**     | **VLAN ID** | **Subnet**          | **Host Range**               | **Purpose**                                  |
|---------------------|-------------|---------------------|------------------------------|----------------------------------------------|
| Sales               | 10          | 192.168.10.0/25    | 192.168.10.1 - 192.168.10.126| Secure access to customer databases.         |
| R&D                 | 20          | 192.168.20.0/25    | 192.168.20.1 - 192.168.20.126| Protect intellectual property and research.  |
| Administration      | 30          | 192.168.30.0/25    | 192.168.30.1 - 192.168.30.126| Manage sensitive employee and financial data.|
| DMZ                 | 40          | 192.168.40.0/25    | 192.168.40.1 - 192.168.40.126| Isolate external-facing servers and services.|

### **3. Routing and Data Flow**
- **Protocol:** Open Shortest Path First (OSPF) for dynamic routing.
- **NAT Implementation:** Masks private IP addresses to enhance internal network security.
- **ACLs:** Restrict inter-departmental traffic and limit unauthorised external access. Example:  
  ```
  ip access-list extended ADMIN_ONLY permit tcp 192.168.30.0 0.0.0.255 192.168.40.0 0.0.0.255 eq 443 deny ip any any
  ```

---

## **Configurations**

### **Router and Switch Configurations**
1. **Router Settings:**
 - **Dynamic Routing:**  
   ```
   router ospf 1
   network 192.168.0.0 0.0.255.255 area 0
   ```
 - **NAT Configuration:**  
   ```
   ip nat inside source list 1 interface GigabitEthernet0/1 overload
   access-list 1 permit 192.168.0.0 0.0.255.255
   ```
 - **Logging:**  
   ```
   logging buffered 4096
   logging trap warnings
   ```

2. **Switch Settings:**
 - **VLAN Assignment:**  
   ```
   vlan 10
   name Sales
   vlan 20
   name R&D
   vlan 30
   name Administration
   vlan 40
   name DMZ
   ```
 - **Inter-VLAN Routing:**  
   ```
   interface vlan10
   ip address 192.168.10.1 255.255.255.128
   ```

3. **VPN Gateway Configuration:**
 - **TLS Encryption for VPN:**  
   ```
   crypto isakmp policy 10
   encryption aes
   hash sha256
   group 14
   authentication pre-share
   ```
 - **VPN Tunnel Policies:**  
   ```
   crypto ipsec transform-set ESP-AES-SHA esp-aes esp-sha-hmac
   ```
 - **Clientless VPN:** Configured for departmental access with defined ACLs to limit resources.

---

## **Security Controls**

### **1. Access Management**
- **RBAC (Role-Based Access Control):**
- Departmental roles are assigned access to specific VLANs.
- Administrator roles are given elevated privileges with MFA enforcement.
- **SSH and Secure Access:**
- SSH version 2 is enforced for secure device management.
- Configured ACLs restrict SSH access to specific IP ranges:  
  ```
  access-list 2 permit 192.168.30.0 0.0.0.255
  line vty 0 4
  transport input ssh
  access-class 2 in
  ```

### **2. Encryption**
- **TLS 1.3:** Applied for secure communication between remote users and internal servers.
- **AES-256:** Configured for VPN traffic and data at rest on file servers.

### **3. Firewall and DMZ Policies**
The **Demilitarised Zone (DMZ)** hosts critical services such as the web server, mail server, and database server. Firewall rules are applied to isolate the DMZ from internal and external networks.  
- **Inbound Rules:** Allow only HTTPS, SSH, and VPN connections to DMZ servers.  
  ```
  ip access-list extended DMZ_INBOUND permit tcp any host 192.168.40.2 eq 443 permit tcp any host 192.168.40.3 eq 22 deny ip any any
  ```
- **Outbound Rules:** Restrict DMZ servers to communicate only with external client IPs for service requests.  
  ```
  ip access-list extended DMZ_OUTBOUND permit tcp host 192.168.40.2 any eq 443 deny ip any any
  ```

---

## **Learning Outcomes**

1. Gained hands-on experience in designing, configuring, and implementing a secure corporate network using **Cisco Packet Tracer**.
2. Developed expertise in VLAN segmentation, dynamic routing protocols, and NAT configurations.
3. Strengthened understanding of role-based access control (RBAC), encryption protocols, and endpoint security measures.
4. Improved incident response capabilities through SIEM integration and IDS/IPS deployment for real-time anomaly detection.
5. Enhanced ability to implement firewall rules and DMZ isolation to protect critical services from unauthorised access.

---

## **Conclusion and Recommendations**

This project demonstrates the successful design and implementation of a scalable and secure corporate network. By incorporating industry-standard practices and leveraging tools such as **Cisco Packet Tracer**, the network ensures robust security, operational efficiency, and regulatory compliance.

### **Key Highlights:**
- **Layered Defence:** Comprehensive security controls, including VLAN segmentation, encryption, and access management.
- **DMZ Protection:** Isolation of critical services with tailored firewall rules and ACLs.
- **Monitoring and Incident Response:** Proactive anomaly detection using SIEM tools and IDS/IPS systems.

### **Future Recommendations:**
1. Deploy advanced anomaly detection algorithms for enhanced threat detection and mitigation.
2. Transition to WPA3-Enterprise for improved wireless security across departments.
3. Implement zero-trust principles, ensuring continuous verification of access requests.

---

