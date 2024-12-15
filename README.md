# Youssef-Hagar
## Objective
Build an Active Directory home lab using Windows Server, Windows 10, and pfSense to monitor network traffic activity, with Kali Linux for attack simulations.
### Skills Learned
- Active Directory Management and Domain Configuration
- Network architecture and setting up a network
- Using different operating systems and joining a domain
- 
### Tools Used
- VirtualBox as a hypervisor for the virtual environment
- Windows Server for as Domain Controller
- Windows 10 as a client for the domain, and a target machine for exploitation
- Kali Linux for penetration testing

### Steps
1. On VirtualBox, create all virtual machines by assigning the appropriate amount of RAM and CPU for each device. Also, configure the NIC adapter to the Internal network with the exception of adding an extra adapter on pfSense set to NAT, to communicate with the internet.
2. Set up the pfSesne WAN side to use DHCP to get an IP from your home router, and set up the LAN side to act as a DHCP server. We will use 192.168.100.0/24 for our lab (the DHCP server can also be set up later using GUI).
3. Set up Windows Server with security best practices (non-default username and complex password), then assign a static IP address (192.168.100.2) with the right network mask and gateway.
4. Add Active Directory Services in the Server Manager then promote the server as a Domain Controller by setting up the domain name. Populate the users' list in Server Manager.
5. Set up the rest of the virtual machines, they should all get IP addresses automatically via DHCP, then join the domain using the created users.
6. Enjoy your lab!
