# Secure_Healthcare_Information_Network_System_Design_And_Implementation






I put several networking concepts such as Voice Over IP (VoIP), Spanning Tree Protocol (STP), Dynamic Host Configuration Protocol(DHCP), Subnetting, IP addressing, Secure Shell(SSH), Routers, Switches, Hierarchical Network Design, VLANs, Inter-VLAN Routing, Access Lists, Open Source Path First (OSPF), Static Routing, Wireless Access Points, Wireless Controller, Ether Channel and Firewall into practice by implementing a modest-level networking project based on a case study.







Dr.Devi ShettyLabs Limited is an Indian Healthcare Service Provider specializing in diagnostic and related healthcare tests. Headquartered in Mumbai, the company conducts tests on blood, urine and various human bodily tissues. It strategically employs information technology to digitize and securely access and market its services. The companys' offices are located on the 35th, 36th and 37th floor of the Great Namaste Tower. On the 35th floor, you'll find the Pharmacy and Medical Labs, serving approxiamately 200 users, along with the Reception and Guest Area accommodating around 1000 users. The 36th floor houses the Doctors and Consultancy Department, catering to about 200 users, and also manages Procurement, HR and Finance operations for 300 users. The 37th floor is divided between Internal Auditors and Corporate functions, involving around 120 users, and an entire IT Team consisting of 300 users. The IT department is further structured into various teams, including Brand and Digital Marketing. IT Support, System/Network Admin, Network Security Engineers, Cybersecurity Analysts, Software Engineers, Cloud Engineers and IT Management. Recognizing substantial growth potential, the company anticipates that the user count for each department will double within two years, necessitating a focus on scalibility during the design and implementation phases.








As an integral part of the companys' ICT infrastructure, the following components have been incorporated:






a) Internet Service Provider (ISP) :- The company has established a subscription with Airtel to ensure internet connectivity.






b) Network Security :- A Cisco ASA Firewall from the 5500-X series has been acquired to enhance network security.






c) Switching Infrastructure :- The network includes two catalyst 3850 48-Port Switches, eight catalyst 2960 48-Port Switches and two 2960 24-Port Switches to ensure robust local network connectivity.






d) Network Routing :- A Cisco WAN Router has been deployed to faciliate efficient data routing within the network. NOTE : For some reason, this router will be used for VoIP services.






e) Server Hardware and Virtualization :- Two HP ProLiant DL38 Gen10 servers will be utilized for virtulization through the VMWare ESXi hypervisor. They will host multiple virtual machines, including a Red Hat Directory Server responsible for managing user information in an LDAP-based directory. This server will handle DNS services and IPv4 address allocation for DHCP hosts. The two servers are used for fail-over purpose.





f) Internal Servers :- Internally hosted servers include a Healthcare Information System, Email Server and File Server, ensuring data accessibility and security.





g) Storage :- Two storage devices, NetApp product will be used to facilitate storage of resources.





h) Voice and Wireless Infrastructure :- Cisco Voice Gateways will be employed for VoIP and telephony services. Additionally, a Cisco Wireless LAN Controller (WLC) and ten Lightweight Access Points (LAPs) will centralize the management of the wireless network.




Cloud Computing as an important technology is used to connect clients accross the world to the company services and resources thus the helthcare system is linked to the AWS cloud platform to facilitate service delivery thus this is one of the core business functions of the firm. The developers and cloud engineers use several cloud resources to ensure seamless business continuity. The proposed network should allow the team access to these resources.







Due to security requirements, it has been decided that all LAN, WLAN and VoIP users will be on a seperate network segment within the same local area network. The firewall will be used to set security zones and filter traffic that moves in and out of the zones based on the configured inspection policies.






You have been hired as a network security engineer to design the network according to the requirements set by the senior management. You will consult an appropriate robust network design model to meet the design requirements. You are required to design and implement a secured, reliable, scalable and robust network system that is paramount to safeguarding the Confidentially, Integraity and Availability of the data and communication.








Requirements :






The company places a strong emphasis on achieving top-tier performance, redudancy, scalibility and availability  within the network infrastructure. As such, your task involves creating a comprehensive network design and executing its implementation. To facilitate this endeavor, the company has designated specific IP address range.






-> WLAN :- The WLAN Network network will operate within the IP address range of 10.10.0.0/16






-> LAN :- For the local area network (LAN), the IP address range of 192.168.0.0/20 has been allocated.






-> Voice :- The Voice network will utilize the IP address range of 172.16.0.0/20.





-> DMZ :- The Demilitarized Zone (DMZ) will be assigned IP address form the range 10.20.20.0/26






-> Public Addresses :- Public IP addresses from the range 197.200.100.0 have been allocated for external facing services, ensuring a visible and accessible presence on the internet.







Technical Requirements : 





a) Design Tool => Utilize Cisco Packet Tracer for designing and implementing the network solution.







b) Hierarchical Design => Implement a hierarchical model that incorprates redudancy for enhanced network resilience.






c) ISPs => Establish connectivity to an Airtel ISP Router within the network infrastructure.







d) WLC => Ensure that each department is equipped with a Wireless Access Point (WAP) to provide WiFi access to employees, corporate users, external auditors and guests, all centrally managed by a Wireless LAN Controller (WLC).






e) VoIP => Deploy Ip Phones in each department to support Voice over IP (VoIP) communication.






f) VLAN => Maintain VLANs with the following IDs :- 10 for LAN, 50 for WLAN and 99 for VoIP accross the entire network.






g) EtherChannel => Implement the Link Aggregration Control Protocol (LACP) for EtherChannel configuration, enhancing link aggregration efficiency.







h) STP PortFast and BPDUguard => Configure Spanning Tree Protocol (STP) PortFast and BPDUguard to expedite port transitions from blocking to forwading states.








i) Subnetting => Utilize subnetting techniques to allocate the appropriate number of IP addresses to each network group.







j) Basic Settings => Configure fundamental device settings, including hostnames, console passwords, enable passwords, banner messages, password encryption and disable IP domain lookup.







k) Inter-VLAN Routing => Enable devices in all departments to communicate with one another by configuring the respective multilayer switch for inter-VLAN routing.






l) Core Switch => Assign IP addresses to Mutilayer Switches to enable both routing and switching functionalities.







m) DHCP Server => Ensure that all devices in the network (Excluding IP phones) obtain IP addresses dynamically from Active Directory (AD) servers located at the server farm site.







n) Cisco 2811 Router => Deploy a Cisco Catalyst 2811 router capable of supporting telephony service.







o) HSRP => Implement high-availability router protocols such as HSRP to achieve redudancy, load balancing and failover capabilities.







p) Static Addressing => Allocate static IP addresses to devices located in the server room.







q) Telephony Service => Configure Voice over IP (VoIP) on the WAN router and assign dial numbers in the format (3...).







r) Routing Protocols => Utilize Open Shortest Path First (OSPF) as the routing protocol to advertise routes on the firewall, routers and multilayer switches.







s) Standard ACL for SSH => Establish a simple standard Access Control List (ACL) on the VTY line to permit remote administrative tasks via SSH only for the Senior Network Security Engineer PC.








t) Cisco ASA Firewall => Configure default static routes, basic settings, security levels, zones and policies on the Cisco ASA Firewall to define access control and resource utilization within the network.










u) Final Testing => Conduct thorough testing to verify proper communication and ensure that all configured elements function as intended.







Video Demonstration :- https://drive.google.com/file/d/1SiQg2dYcSdJm1aGHzXGRg1CF-9RU5PUR/view?usp=sharing
