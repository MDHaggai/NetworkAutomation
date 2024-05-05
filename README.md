# NetworkAutomation Case Study



A Bank Company Ltd. is a Cameroon-owned company that deals with Banking and Insurance. The company is intending to expand its services across the African continent having the first branch to be located in Yaounde, Cameroon. The company has secured a four-story building to operate within the Camerron capital city. Therefore, the company would like to allow sourcing the knowledge from a Network Expert from t to design and implement their company network. A Network Engineer to take over this role should carefully read down the requirements then model the design and implement the network based on the company's needs. Each floor has departments as provided in the table below.;

![Screenshot 2024-05-05 132804](https://github.com/LKLespa/creative-skills-hub-2/assets/123896407/4106cfd0-1e89-40f0-9f5c-b300cf42cd97)



## Objective: 
Utilize GNS3 for designing and implementing a fully automated network to support an organizational infrastructure with detailed hierarchical network design.

## Tools and Software:
- Modeling Tools:
   Use MS Visio, Visual Paradigm, or Draw.io to visually represent the hierarchical network design.
- Simulation Software:
   Deploy GNS3 for network simulation to ensure effective design and automation.
## Network Configuration and Setup:
- Routing Protocol:
   Implement OSPF for efficient routing and route advertisement across the network.
- Network Segmentation:
  Each department will have a dedicated network segment accommodating approximately 60 users. The server room will act as the central node for network administration and does not require standard user configurations.
- IP Address Management:
   Automate IPv4 address assignment using DHCP. The DHCP servers will be centrally located in the server room for dynamic IP management across all devices.
- Inter-Department Communication:
  Ensure all departmental networks are interconnected, allowing seamless communication between different segments.
- Server Configuration:
 Establish essential services by setting up HTTP and Email servers within the network infrastructure.
## Security and Administration:
- SSH Configuration:
  Enable SSH on all routers to facilitate secure remote logins, configuration updates, and network automation scripts.
- Device Configuration Basics:
 Configure hostnames, line console settings, enable passwords, and banner messages. Implement security measures such as disabling domain IP lookup and encrypting all configured passwords.
- VLAN and Subnetworking:
 Assign each department to a unique VLAN (e.g., VLAN 10, 20, 30, etc.). Perform subnetting based on the provided base address 192.168.10.0, calculating subnet masks, usable IP address ranges, and broadcast addresses for each subnet.
- Port Security:
   Implement switchport security using the sticky MAC address feature and configure violation modes to shutdown upon security breaches.
## Automation and Scripting:
- End Device Configurations:
   Program all end devices from the server room using scripts that assign IP addresses based on the subnetting results.
- Inter-VLAN Routing:
   Configure Multilayer switches with Switch Virtual Interfaces (SVIs) for handling routing between VLANs.
- DHCP Configuration:
  Set up dedicated DHCP servers to automatically distribute IP addresses across the network.
## Testing and Verification:
- Network Communication Tests:
   Conduct thorough tests to verify that all network communications function correctly within and between VLANs. Check the responsiveness of HTTP and Email servers.
- Security Audits:
   Perform security checks to ensure that SSH and port-security configurations meet the organizational security standards.
- Visualization and Reporting:
Network Topology Documentation: Utilize GNS3 to create detailed network topology diagrams that reflect all configurations and setups for record-keeping and troubleshooting.

The network topology below satisfy the user requirements above and everything is verified, tested and working fine. You can get source file (Packet Tracer File) or watch on YouTube below.


